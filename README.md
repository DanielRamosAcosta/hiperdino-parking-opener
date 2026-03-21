# Generador de Tickets de Parking - Hiperdino San Benito

Genera códigos de barras válidos para la salida del parking del Hiperdino de San Benito, La Laguna.

## ¿Cómo funciona?

La app calcula un código de 13 dígitos que codifica la hora de salida con un margen de 20 minutos sobre la hora actual. El código se actualiza en tiempo real cada segundo y se renderiza como un código de barras escaneable por la barrera del parking.

El "número mágico" (0-9) se puede ajustar con los botones `+` y `-` del ticket.

## Desarrollo

```bash
npm install
npm run dev
```

## Tests

```bash
npm test
```

## Deploy

Se despliega automáticamente en GitHub Pages al hacer push a `main`.
