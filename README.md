# CarCare Data Hub (Repositorio Vehicular Descentralizado & Portal B2B)

Motor de datos abierto, portal de talleres aliados ("Cero Teclados") y laboratorio de Machine Learning (`ISU -> XGBoost / Random Survival Forests`) del ecosistema **CarCare AI** en Lima Metropolitana.

Conectado conceptual y técnicamente con el MVP para conductores: [https://carcare-ai-mvp.vercel.app/](https://carcare-ai-mvp.vercel.app/)

## Stack Tecnológico
- **Framework:** Next.js 15 (App Router), React 19, TypeScript (Strict Mode)
- **UI / Estilos:** Tailwind CSS (`#0A0F17` base, `#111827` cards, esmeralda `#10B981`, ámbar `#F59E0B`, rojo `#EF4444`, azul `#3B82F6`)
- **Iconografía:** `lucide-react`
- **Persistencia Híbrida:** `RepositoryContext` sincronizado en tiempo real con `localStorage` + esquema DDL PostgreSQL descargable para **Supabase** y endpoints REST API (`/api/v1/vin/[vin]/compatibility` y `/api/v1/isu/calibrated-weights`).

## Las 5 Vistas Interactivas
1. **Buscador Público "Carfax Peruano" (Trazabilidad por VIN / Placa):** Decodificación OEM, comparativa Odómetro Físico vs. Kilómetros Efectivos (ISU) y línea de tiempo auditable con mediciones físicas en milímetros y evidencia de los 4 hitos QR.
2. **Portal B2B Talleres Aliados (Ingesta "Cero Teclados" + Biblioteca KEDB):** Flujo táctil de 4 hitos sin campos de texto libre para mecánicos en bahía y base de datos de errores conocidos (KEDB) en Lima.
3. **Arquitectura del Repositorio (Triangulación de 3 Capas & Explorador SQL):** Diagrama interactivo de las 3 capas, explorador relacional en vivo de las 5 tablas core, exportador CSV/JSON para ML y modal con el script DDL PostgreSQL (Supabase).
4. **Laboratorio Predictivo (De Reglas ISU a Machine Learning Supervisado):** Simulador interactivo con controles deslizantes ($\alpha_{\text{congestión}}$, $\beta_{\text{topografía}}$, $\gamma_{\text{térmico}}$), comparativa de las 3 etapas evolutivas, curva de probabilidad de supervivencia y botón de ingesta masiva (`+100 auditorías`).
5. **Índice Nacional de Fiabilidad & Puente API:** Ranking empírico de durabilidad OEM vs. Tier-1 (Aisin, Denso, Brembo, Bosch, Mann Filter, Idemitsu) y consola de sincronización JSON en vivo.

## Ejecución Local

```bash
npm install
npm run dev
```

