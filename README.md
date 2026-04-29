# Ejercicio-2.3
ejercicio de poo 2.3

from enum import Enum 

class TipoCom(Enum): 

    GASOLINA = 1 

    BIOETANOL = 2 

    DIESEL = 3 

    BIODIESEL = 4 

    GAS_NATURAL = 5 

class TipoA(Enum): 

    CIUDAD = 1 

    SUBCOMPACTO = 2 

    COMPACTO = 3 

    FAMILIAR = 4 

    EJECUTIVO = 5 

    SUV = 6 


class TipoColor(Enum): 

    BLANCO = 1 

    NEGRO = 2 

    ROJO = 3 

    NARANJA = 4 

    AMARILLO = 5 

    VERDE = 6 

    AZUL = 7 

    VIOLETA = 8 

 
class Automovil: 

 

    def __init__(self, marca, modelo, motor, tipoCombustible, 

                 tipoAutomovil, numeroPuertas, cantidadAsientos, 

                 velocidadMaxima, color): 

 

        self.marca = marca 

        self.modelo = modelo 

        self.motor = motor 

        self.tipoCombustible = tipoCombustible 

        self.tipoAutomovil = tipoAutomovil 

        self.numeroPuertas = numeroPuertas 

        self.cantidadAsientos = cantidadAsientos 

        self.velocidadMaxima = velocidadMaxima 

        self.color = color 

        self.velocidadActual = 0 

 

    def getMarca(self): 

        return self.marca 

 

    def getModelo(self): 

        return self.modelo 

 

    def getMotor(self): 

        return self.motor 

 

    def getTipoCombustible(self): 

        return self.tipoCombustible 

 

    def getTipoAutomovil(self): 

        return self.tipoAutomovil 

 

    def getNumeroPuertas(self): 

        return self.numeroPuertas 

 

    def getCantidadAsientos(self): 

        return self.cantidadAsientos 

 

    def getVelocidadMaxima(self): 

        return self.velocidadMaxima 

 

    def getColor(self): 

        return self.color 

 

    def getVelocidadActual(self): 

        return self.velocidadActual 

 

 

    def setMarca(self, marca): 

        self.marca = marca 

 

    def setModelo(self, modelo): 

        self.modelo = modelo 

 

    def setMotor(self, motor): 

        self.motor = motor 

 

    def setTipoCombustible(self, tipoCombustible): 

        self.tipoCombustible = tipoCombustible 

 

    def setTipoAutomovil(self, tipoAutomovil): 

        self.tipoAutomovil = tipoAutomovil 

 

    def setNumeroPuertas(self, numeroPuertas): 

        self.numeroPuertas = numeroPuertas 

 

    def setCantidadAsientos(self, cantidadAsientos): 

        self.cantidadAsientos = cantidadAsientos 

 

    def setVelocidadMaxima(self, velocidadMaxima): 

        self.velocidadMaxima = velocidadMaxima 

 

    def setColor(self, color): 

        self.color = color 

 

    def setVelocidadActual(self, velocidadActual): 

        self.velocidadActual = velocidadActual 

 

 

    def acelerar(self, incrementoVelocidad): 

        if self.velocidadActual + incrementoVelocidad < self.velocidadMaxima: 

            self.velocidadActual += incrementoVelocidad 

        else: 

            print("No se puede incrementar a una velocidad superior a la máxima del automóvil.") 

 

    def desacelerar(self, decrementoVelocidad): 

        if (self.velocidadActual - decrementoVelocidad) > 0: 

            self.velocidadActual -= decrementoVelocidad 

        else: 

            print("No se puede decrementar a una velocidad negativa.") 

 

    def frenar(self): 

        self.velocidadActual = 0 

 

    def calcularTiempoLlegada(self, distancia): 

        return distancia / self.velocidadActual 

 

    def imprimir(self): 

        print("Marca =", self.marca) 

        print("Modelo =", self.modelo) 

        print("Motor =", self.motor) 

        print("Tipo de combustible =", self.tipoCombustible.name) 

        print("Tipo de automóvil =", self.tipoAutomovil.name) 

        print("Número de puertas =", self.numeroPuertas) 

        print("Cantidad de asientos =", self.cantidadAsientos) 

        print("Velocidad máxima =", self.velocidadMaxima) 

        print("Color =", self.color.name) 

if __name__ == "__main__": 

 

    auto1 = Automovil( 

        "Ford", 

        2018, 

        3, 

        TipoCom.DIESEL, 

        TipoA.EJECUTIVO, 

        5, 

        6, 

        250, 

        TipoColor.NEGRO 

    ) 

 

    auto1.imprimir() 

 

    auto1.setVelocidadActual(100) 

    print("Velocidad actual =", auto1.velocidadActual) 

 

    auto1.acelerar(20) 

    print("Velocidad actual =", auto1.velocidadActual) 

 

    auto1.desacelerar(50) 

    print("Velocidad actual =", auto1.velocidadActual) 

 

    auto1.frenar() 

    print("Velocidad actual =", auto1.velocidadActual) 

 

    auto1.desacelerar(20) 
