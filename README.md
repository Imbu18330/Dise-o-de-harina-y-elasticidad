# Crear un dataframe con los datos del experimento
datos <- data.frame(
  Tipo_de_Harina = factor(rep(c("Trigo", "Coco", "Quinua"), each = 6)),
  Cantidad_de_Agua = factor(rep(rep(c("Baja", "Alta"), each = 3), times = 3)),
  Elasticidad = c(4, 5, 4, 5, 5, 5, 2, 3, 2, 3, 3, 2, 3, 3, 2, 3, 3, 4)
)

# Mostrar los datos
print(datos)
# Realizar el ANOVA
modelo <- aov(Elasticidad ~ Tipo_de_Harina * Cantidad_de_Agua, data = datos)

# Mostrar el resumen del ANOVA
summary(modelo)

