---
title: Common-Shader Core
description: Common-Shader Core
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e27ebe7d908c473890ac5b851eac3e0bc840c859
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855723"
---
# <a name="common-shader-core"></a>Common-Shader Core

In Shader Model 4 implementieren alle Shader-Stufen die gleiche Basisfunktionalität mithilfe eines gemeinsamen shaderkerns. Außerdem bieten jede der drei Shader-Stufen (Scheitelpunkt, Geometrie und Pixel) Funktionen, die für jede Phase eindeutig sind, z. b. die Möglichkeit, neue primitive aus der Geometrie-Shader-Phase zu generieren oder ein bestimmtes Pixel in der Pixel-Shader-Stufe zu verwerfen. Das folgende Diagramm zeigt, wie Daten durch eine Shader-Stufe und die Beziehung des Common-Shader-Kerns mit Shader-Speicherressourcen fließen.

![Diagramm des Datenflusses in einer Shader-Phase](images/d3d10-shader-unit.png)

-   **Eingabedaten**: ein Vertex-Shader empfängt seine Eingaben aus der Eingabe Assembler-Stufe. Geometry-und Pixel-Shader erhalten Ihre Eingaben aus der vorherigen Shader-Stufe. Weitere Eingaben umfassen eine [System Wert Semantik](dx-graphics-hlsl-semantics.md), die von der ersten Einheit in der Pipeline, auf die Sie anwendbar sind, genutzt werden kann.
-   **Ausgabedaten**: Shaders generieren Ausgabe Ergebnisse, die an die nachfolgende Phase in der Pipeline übermittelt werden. Bei einem Geometry-Shader kann die Menge an Daten, die von einem einzelnen Aufruf ausgegeben werden, variieren. Einige Ausgaben werden vom Common-Shader-Kern (z. b. Scheitelpunkt Position und Renderziel-Array-Index) interpretiert, andere sind so konzipiert, dass Sie von einer Anwendung interpretiert werden.
-   **Shadercode: Shader** können aus dem Arbeitsspeicher lesen, die arithmetischen Operationen für Vektor Gleit Komma-und ganzzahlige Operationen oder Fluss Steuerungs Vorgänge durchführen. Es gibt keine Beschränkung für die Anzahl der Anweisungen, die in einem Shader implementiert werden können.
-   **Samplers**: Samplers definieren, wie Texturen von Beispielen und Filtern gefiltert werden. Bis zu 16 samplz können gleichzeitig an einen Shader gebunden werden.
-   **Texturen**: Texturen können mithilfe von Samplern gefiltert werden, oder Sie können direkt mit der systeminternen [Load](dx-graphics-hlsl-to-load.md) -Funktion gelesen werden.
-   **Puffer**: Puffer werden nie gefiltert, können jedoch direkt mit der systeminternen [Load](dx-graphics-hlsl-to-load.md) -Funktion aus dem Arbeitsspeicher aus dem Arbeitsspeicher gelesen werden. So viele wie 128 Textur-und Puffer Ressourcen (kombiniert) können gleichzeitig an einen Shader gebunden werden.
-   **Konstante Puffer**: Konstante Puffer werden für Shader-Konstantenvariablen optimiert. Bis zu 16 Konstante Puffer können gleichzeitig an eine Shader-Phase gebunden werden. Sie sind für häufigere Updates von der CPU konzipiert. Daher haben Sie zusätzliche Größen-, Layout-und Zugriffsbeschränkungen.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> In Direct3D 9 besaß jede Shader-Einheit eine einzelne, kleine Konstante Registrierungsdatei, um alle Konstanten shadervariablen zu speichern. Wenn alle Shader mit diesem eingeschränkten Konstanten Raum untergebracht werden, ist eine häufige Wiederverwendung von Konstanten durch die CPU erforderlich.<br/> In Direct3D 10 werden Konstanten in unveränderlichen Puffer im Arbeitsspeicher gespeichert und wie jede andere Ressource verwaltet. Es gibt keine Beschränkung für die Anzahl der Konstanten Puffer, die eine Anwendung erstellen kann. Durch die Organisation von Konstanten in Puffern nach Aktualisierungs-und Verwendungs Häufigkeit kann die Menge an Bandbreite, die zum Aktualisieren von Konstanten für alle Shader erforderlich ist, erheblich reduziert werden.<br/> |



 

## <a name="integer-and-bitwise-support"></a>Ganzzahlige und bitweise Unterstützung

Der gemeinsame Shader-Kern bietet einen vollständigen Satz von IEEE-kompatiblen, ganzzahligen 32-Bit-und bitweisen Vorgängen. Diese Vorgänge ermöglichen eine neue Klasse von Algorithmen in Grafikhardware Beispielen, einschließlich Komprimierungs-und Komprimierungs Techniken, FFTs und der programmflusssteuerung für das Bitfeld.

Die Datentypen " **int** " und " **uint** " in Direct3D 10 HLSL sind in der Hardware 32-Bit-Ganzzahlen zugeordnet.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> In Direct3D 9 werden Datenstrom Eingaben, die in HLSL als Integer gekennzeichnet sind, als Gleit Komma interpretiert. In Direct3D 10 werden als Integer markierte streameingaben als 32-Bit-Ganzzahl interpretiert.<br/> Außerdem sind boolesche Werte jetzt alle Bits festgelegt, oder alle Bits sind nicht festgelegt. Daten, die in **bool** konvertiert werden, werden als true interpretiert, wenn der Wert nicht mit 0,0 f übereinstimmt (sowohl positive als auch negative Null sind zulässig), andernfalls false.<br/> |



 

## <a name="bitwise-operators"></a>Bitweise Operatoren

Der Common Shader Core unterstützt die folgenden bitweisen Operatoren:



| Operator  | Funktion          |
|-----------|-------------------|
| ~         | Logisches NOT       |
| <<  | Nach links verschieben        |
| >>  | Rechte Verschiebung       |
| &         | Logisches UND       |
| \|        | Logisches ODER.        |
| ^         | Logisches XOR       |
| <<= | Left Shift gleich  |
| >>= | Rechtsverschiebung gleich |
| &=        | Und gleich         |
| \|=       | Oder gleich          |
| ^=        | XOR-gleich         |



 

Bitweise Operatoren sind so definiert, dass Sie nur für die Datentypen **int** und **uint** verwendet werden. Der Versuch, bitweise Operatoren für die Datentypen **float** oder **struct** zu verwenden, führt zu einem Fehler. Bitweise Operatoren folgen in Bezug auf andere Operatoren der gleichen Rangfolge wie C.

## <a name="binary-casts"></a>Binäre Umwandlungen

Durch Umwandeln zwischen einer Ganzzahl und einem Gleit kommatyp wird der numerische Wert nach C-abkürzen konvertiert. Das Umwandeln eines Werts aus **einer Gleit** Komma Zahl **in einen** ganzzahligen Wert in einen **float** -Wert ist eine verlustfreie Konvertierung, die von der Genauigkeit des Ziel Datentyps abhängt. Im folgenden finden Sie einige der Konvertierungs Funktionen: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).

Binäre Umwandlungen können auch mit systeminternen HLSL-Funktionen ausgeführt werden. Diese bewirken, dass der Compiler die Bit-Darstellung einer Zahl in den Ziel Datentyp uminterpretiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





