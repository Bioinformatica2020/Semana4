# Semana4

## Código para mejorar la visualización de gráficos de barras

```
# Gráfico de barras horizontal

fig, ax = plt.subplots(figsize=(5,8), linewidth= 5)

for i, j in zip(frecuencia2[0], # Columna 0 del DataFrame frecuencia2
                frecuencia2[1]): # Columna 1 del DataFrame frecuencia2
    ax.barh('$\it{'+i+'}$', # etiquetas del eje x, en itálica
            j, # valores del eje y
             color= 'black', # color 
             align='center', # alineamiento de las barras, la otra opción 'edge'
             height= 0.8, # grosor de las barras
            linewidth = 0, # ancho del borde de las barras
             alpha = 0.7, # transparencia
            edgecolor= 'black') # color del borde de las barras

ax.spines['right'].set_visible(False) # oculta la linea derecha
ax.spines['left'].set_visible(False) # oculta la linea izquierda
ax.spines['top'].set_visible(False) # oculta la linea superior 
ax.spines['bottom'].set_position(('data',-0.6)) # separación entre la primer barra y el eje x

ax.xaxis.set_tick_params(labelsize=10) # tamaño de letra del eje x
ax.yaxis.set_tick_params(labelsize=12) # tamaño de letra del eje y
ax.set_xlabel("Número de géneros",size= 15) # título y tamaño para el eje x
ax.set_ylabel("Géneros", size= 15) # título y tamaño para el eje y
ax.set_title('Frecuencia', size= 20) # Título del gráfico

# si quieres salvar el gráfico activa la siguiente línea, y vuelve a correr la celda
#fig.savefig('../salidas/Generos_Barras.png',dpi = 600, bbox_inches='tight')

plt.show()
```
<img src="https://raw.githubusercontent.com/Bioinformatica2020/Anexos/master/Generos_Barras.png" width = 50%>

---
---

##### `"Si lo oigo lo olvido, si lo veo lo entiendo, si lo hago lo aprendo"` 
##### Confucio
