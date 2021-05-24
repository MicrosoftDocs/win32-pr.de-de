---
title: Verwenden von System-Generated Werten
description: Vom System generierte Werte werden von der IA-Phase generiert (basierend auf der vom Benutzer bereitgestellten Eingabesemantik), um bestimmte Effizienz bei Shadervorgängen zu ermöglichen.
ms.assetid: eed1e377-4b0e-4958-b6d4-945b2a952ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdc723d335fd78277051099ec05b43ed954174d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335204"
---
# <a name="using-system-generated-values"></a>Verwenden von System-Generated Werten

Vom System generierte Werte werden von der IA-Phase generiert (basierend auf der vom Benutzer [bereitgestellten Eingabesemantik),](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)um bestimmte Effizienz bei Shadervorgängen zu ermöglichen.

Durch das Anfügen von Daten, z. B. einer Instanz-ID (für VS sichtbar), einer Vertex-ID (sichtbar für VS) oder einer primitiven ID (sichtbar für GS/PS), kann eine nachfolgende Shaderphase nach diesen Systemwerten suchen, um die Verarbeitung in dieser Phase zu optimieren. Beispielsweise kann die VS-Phase nach der Instanz-ID suchen, um zusätzliche Pro-Scheitelpunkt-Daten für den Shader zu greifen oder andere Vorgänge auszuführen. die GS- und PS-Phasen können die primitive ID verwenden, um daten pro Primitive auf die gleiche Weise zu greifen.

-   [VertexID](#vertexid)
-   [PrimitiveID](#primitiveid)
-   [InstanceID](#instanceid)
-   [Beispiel](#example)
-   [Verwandte Themen](#related-topics)

## <a name="vertexid"></a>VertexID

Eine Scheitelpunkt-ID wird von jeder Shaderstufe verwendet, um jeden Scheitelpunkt zu identifizieren. Es handelt sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, deren Standardwert 0 ist. Sie wird einem Scheitelpunkt zugewiesen, wenn der Primitive von der IA-Phase verarbeitet wird. Fügen Sie die Scheitelpunkt-ID-Semantik an die Shadereingabedeklaration an, um die IA-Stufe zu informieren, eine Pro-Scheitelpunkt-ID zu generieren.

Die IA fügt jedem Scheitelpunkt eine Scheitelpunkt-ID zur Verwendung durch Shaderstufen hinzu. Für jeden Draw-Aufruf wird die Scheitelpunkt-ID um 1 erhöht. Bei indizierten Zeichnen-Aufrufen wird die Anzahl auf den Startwert zurückgesetzt. Für [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) und [**ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced)stellt die Vertex-ID den Indexwert dar. Wenn die Scheitelpunkt-ID überläuft (überschreitet 2bereit– 1), wird sie auf 0 umbrochen.

Für alle primitiven Typen ist Scheitelpunkten eine Scheitelpunkt-ID zugeordnet (unabhängig von der Adjazenz).

## <a name="primitiveid"></a>PrimitiveID

Jede Shaderstufe verwendet eine primitive ID, um die einzelnen Primitiven zu identifizieren. Es handelt sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, deren Standardwert 0 ist. Sie wird einem Primitiv zugewiesen, wenn der Primitive von der IA-Phase verarbeitet wird. Um die IA-Phase zu informieren, eine primitive ID zu generieren, fügen Sie die Primitive-ID-Semantik an die Shadereingabedeklaration an.

Die IA-Phase fügt jedem Primitiv eine primitive ID hinzu, die vom Geometrie-Shader oder der Pixel-Shader-Stufe verwendet werden kann (je nachdem, welcher Schritt nach der IA-Phase die erste aktive Phase ist). Für jeden indizierten Draw-Aufruf wird die primitive ID um 1 erhöht. Die primitive ID wird jedoch auf 0 zurückgesetzt, wenn eine neue Instanz beginnt. Alle anderen Draw-Aufrufe ändern den Wert der Instanz-ID nicht. Wenn die Instanz-ID überläuft (überschreitet 2* bis 1), wird sie auf 0 (0) umbruch.

Die Pixel-Shader-Stufe verfügt nicht über eine separate Eingabe für eine primitive ID. Jede Pixel-Shadereingabe, die eine primitive ID angibt, verwendet jedoch einen konstanten Interpolationsmodus.

Es gibt keine Unterstützung für das automatische Generieren einer primitiven ID für angrenzende Primitive. Bei primitiven Typen mit Adjazienz, z. B. einem Dreiecksstreifen mit Adjakenz, wird eine primitive ID nur für die inneren Primitiven (die nicht angrenzenden Primitiven) beibehalten, genau wie die Gruppe primitiver Typen in einem Dreiecksstreifen ohne Adjakenz.

## <a name="instanceid"></a>InstanceID

Eine Instanz-ID wird von jeder Shaderstufe verwendet, um die Instanz der Geometrie zu identifizieren, die gerade verarbeitet wird. Es handelt sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, deren Standardwert 0 ist.

Die IA-Phase fügt jedem Scheitelpunkt eine Instanz-ID hinzu, wenn die Vertex-Shadereingabedeklaration die Instanz-ID-Semantik enthält. Für jeden indizierten Draw-Aufruf wird die Instanz-ID um 1 erhöht. Alle anderen Draw-Aufrufe ändern den Wert der Instanz-ID nicht. Wenn die Instanz-ID überläuft (überschreitet 2* bis 1), wird sie auf 0 (0) umbrechen.

## <a name="example"></a>Beispiel

Die folgende Abbildung zeigt, wie Systemwerte an einen instanziierten Dreiecksstreifen in der IA-Phase angefügt werden.

![Abbildung der Systemwerte für einen Instanzdreieckstreifen](images/d3d10-ia-example.png)

Diese Tabellen enthalten die Systemwerte, die für beide Instanzen desselben Dreiecksstreifens generiert wurden. Die erste Instanz (Instanz U) wird blau angezeigt, die zweite Instanz (Instanz V) grün. Die durchgezogenen Linien verbinden die Scheitelpunkte in den Primitiven, die gestrichelten Linien verbinden die angrenzenden Scheitelpunkte.

Die folgenden Tabellen zeigen die vom System generierten Werte für die Instanz U.



| Scheitelpunktdaten    | C, U | D, U | E, U | Fick dich | G, U | H,U | I,U | J, U | K, U | L,U |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |



 



|                 | Wert    | Wert    | Wert    |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 0   | 0   | 0   |



 

Die folgenden Tabellen zeigen die vom System generierten Werte für die Instanz V.



| Scheitelpunktdaten    | C, V | D, V | E, V | F,V | G,V | H,V | I,V | J,V | K,V | L,V |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |



 



|                 |Wert     | Wert    |  Wert   |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 1   | 1   | 1   |



 

Der Eingabe-Assembler generiert die IDs (Scheitelpunkt, Primitiv und Instanz). Beachten Sie auch, dass jede Instanz eine eindeutige Instanz-ID erhält. Die Daten enden mit dem Striptrip, der jede Instanz des Dreiecksstreifens trennt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eingabe-Assembler-Phase](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 