---
title: Verwenden von System-Generated Werten
description: Vom System generierte Werte werden von der IA-Phase (basierend auf der vom Benutzer bereitgestellten Eingabe Semantik) generiert, um bestimmte Effizienz bei shadervorgängen zu ermöglichen.
ms.assetid: eed1e377-4b0e-4958-b6d4-945b2a952ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d484a42992206cb04aaef8fdd8ebaef6e08d7f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039261"
---
# <a name="using-system-generated-values"></a>Verwenden von System-Generated Werten

Vom System generierte Werte werden von der IA-Phase (basierend auf der vom Benutzer bereitgestellten Eingabe [Semantik](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) generiert, um bestimmte Effizienz bei shadervorgängen zu ermöglichen.

Durch das Anfügen von Daten, z. b. eine Instanz-ID (sichtbar an vs), eine Scheitelpunkt-ID (sichtbar für vs) oder eine primitive ID (sichtbar für GS/PS), kann eine nachfolgende Shader-Phase nach diesen System Werten suchen, um die Verarbeitung in dieser Phase zu optimieren. Beispielsweise kann in der vs-Phase nach der Instanz-ID gesucht werden, um zusätzliche pro-Vertex-Daten für den Shader zu erfassen oder um andere Vorgänge auszuführen. in den GS-und PS-Phasen kann die primitive ID verwendet werden, um einzelne Daten auf die gleiche Weise zu erfassen.

-   [Vertexid](#vertexid)
-   [Primitiveid](#primitiveid)
-   [InstanceID](#instanceid)
-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="vertexid"></a>Vertexid

Eine Scheitelpunkt-ID wird von jeder Shader-Stufe verwendet, um jeden Scheitelpunkt zu identifizieren. Dabei handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, deren Standardwert 0 ist. Sie wird einem Scheitelpunkt zugewiesen, wenn die primitive von der IA-Phase verarbeitet wird. Fügen Sie die Vertex-ID-Semantik an die shadereingabedeklaration an, um die IA-Phase anzuweisen, eine pro-Vertex-ID

Die IA fügt jedem Scheitelpunkt eine Scheitelpunkt-ID zur Verwendung in Shader-Stufen hinzu. Für jeden zeichnen-Befehl wird die Vertex-ID um 1 erhöht. Über indizierte zeichnen-Aufrufe wird die Anzahl zurück auf den Startwert zurückgesetzt. Für [**Verknüpfung id3d11devicecontext aus::D rawindebug**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) und [**Verknüpfung id3d11devicecontext aus::D rawindexedinstanxed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced)stellt die Scheitelpunkt-ID den Indexwert dar. Wenn die Scheitelpunkt-ID überläuft (überschreitet 2 ³ ² – 1), wird Sie auf 0 (null) umschlossen.

Für alle primitiven Typen sind Scheitel Punkte eine Scheitelpunkt-ID zugeordnet (unabhängig von der Verwendung).

## <a name="primitiveid"></a>Primitiveid

Eine primitive ID wird von jeder Shader-Stufe verwendet, um die einzelnen primitiven zu identifizieren. Dabei handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, deren Standardwert 0 ist. Sie wird einem primitiven zugewiesen, wenn die primitive von der IA-Phase verarbeitet wird. Fügen Sie die primitive-ID-Semantik an die Shader-Eingabe Deklaration an, um die IA-Phase zu informieren und eine primitive ID zu generieren.

In der IA-Phase wird jedem primitiven eine primitive ID für die Verwendung durch den Geometry-Shader oder die Pixel-Shader-Phase hinzugefügt (je nachdem, welche erste Stufe nach der IA-Phase aktiv ist). Für jeden indizierten Draw-Aufruf wird die primitive ID um 1 erhöht. die primitive ID wird jedoch immer auf 0 zurückgesetzt, wenn eine neue Instanz beginnt. Alle anderen Draw-Aufrufe ändern den Wert der Instanz-ID nicht. Wenn die Instanz-ID überläuft (überschreitet 2 ³ ² – 1), wird Sie auf 0 (null) umschlossen.

Die Pixel-Shader-Stufe hat keine separate Eingabe für eine primitive ID. Allerdings wird für jede Pixel-Shader-Eingabe, die eine primitive ID angibt, ein konstanter Interpolations Modus verwendet.

Es gibt keine Unterstützung für das automatische Erstellen einer primitiven ID für benachbarte primitive. Bei primitiven Typen, wie z. b. einem Dreiecks Streifen mit der Verwendung, wird eine primitive ID nur für die inneren primitiven (die nicht angrenzenden primitiven) beibehalten, genauso wie der Satz von primitiven in einem Dreiecks Band ohne jegliche Notwendigkeit.

## <a name="instanceid"></a>InstanceID

Eine Instanz-ID wird von jeder Shader-Phase verwendet, um die Instanz der Geometrie zu identifizieren, die gerade verarbeitet wird. Dabei handelt es sich um eine 32-Bit-Ganzzahl ohne Vorzeichen, deren Standardwert 0 ist.

Die IA-Phase fügt jedem Scheitelpunkt eine Instanz-ID hinzu, wenn die Vertex-Shader-Eingabe Deklaration die Semantik der Instanz-ID enthält. Für jeden indizierten zeichnen-Befehl wird die Instanz-ID um 1 erhöht. Alle anderen Draw-Aufrufe ändern den Wert der Instanz-ID nicht. Wenn die Instanz-ID überläuft (überschreitet 2 ³ ² – 1), wird Sie auf 0 (null) umschlossen.

## <a name="example"></a>Beispiel

In der folgenden Abbildung wird gezeigt, wie System Werte an einen in der IA-Phase angefügten Dreiecks Streifen angefügt werden.

![Abbildung der System Werte für einen instanziierten Dreiecks Streifen](images/d3d10-ia-example.png)

In diesen Tabellen werden die für beide Instanzen desselben Dreiecks Streifens generierten System Werte angezeigt. Die erste Instanz (Instanz U) ist blau dargestellt, die zweite Instanz (Instanz V) ist grün dargestellt. Die durch gestrichelten Linien verbinden die Scheitel Punkte in den primitiven, die gestrichelten Linien verbinden die angrenzenden Scheitel Punkte.

In den folgenden Tabellen sind die vom System generierten Werte für die Instanz U aufgeführt.



| Scheitelpunkt Daten    | C, U | D, U | E, U | F, U | G, U | H, U | I, U | J, U | K, U | L, U |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **Vertexid**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |



 



|                 |     |     |     |
|-----------------|-----|-----|-----|
| **Primitiveid** | 0   | 1   | 2   |
| **InstanceID**  | 0   | 0   | 0   |



 

In den folgenden Tabellen sind die vom System generierten Werte für die Instanz V aufgeführt.



| Scheitelpunkt Daten    | C, V | D, V | E, V | F, V | G, V | H, V | I, V | J, V | K, V | L, V |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **Vertexid**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |



 



|                 |     |     |     |
|-----------------|-----|-----|-----|
| **Primitiveid** | 0   | 1   | 2   |
| **InstanceID**  | 1   | 1   | 1   |



 

Der Eingabe Assembler generiert die IDs (Scheitelpunkt, primitiv und Instanz); Beachten Sie auch, dass jeder Instanz eine eindeutige Instanz-ID zugewiesen wird. Die Daten enden mit dem Strip-Cut, der die einzelnen Instanzen des Dreiecks Streifens trennt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eingabe-Assembler-Phase](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 