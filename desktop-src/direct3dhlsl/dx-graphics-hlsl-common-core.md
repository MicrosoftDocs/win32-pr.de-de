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
ms.openlocfilehash: 9c2d1851025cb051a21a997f5e3a4987d3b6309e148248b3ea55c6b9ca6ad31c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950480"
---
# <a name="common-shader-core"></a>Common-Shader Core

In ShaderModell 4 implementieren alle Shaderstufen die gleiche Basisfunktionalität mit einem gemeinsamen Shaderkern. Darüber hinaus bietet jede der drei Shaderstufen (Scheitelpunkt, Geometrie und Pixel) funktionen, die für jede Stufe spezifisch sind, z. B. die Möglichkeit, neue Primitive aus der Geometrie-Shaderstufe zu generieren oder ein bestimmtes Pixel in der Pixelschattenstufe zu verwerfen. Das folgende Diagramm zeigt, wie Daten durch eine Shaderphase fließen, und die Beziehung zwischen dem gemeinsamen Shaderkern und Shaderspeicherressourcen.

![Diagramm des Datenflusses in einer Shaderphase](images/d3d10-shader-unit.png)

-   **Eingabedaten:** Ein Vertex-Shader empfängt seine Eingaben aus der Eingabe-Assemblerphase. Geometry- und Pixel-Shader erhalten ihre Eingaben aus der vorherigen Shaderphase. Weitere Eingaben umfassen [die Systemwertsemantik,](dx-graphics-hlsl-semantics.md)die von der ersten Einheit in der Pipeline verwendet werden kann, auf die sie anwendbar sind.
-   **Ausgabedaten:** Shader generieren Ausgabeergebnisse, die an die nachfolgende Phase in der Pipeline übergeben werden. Bei einem Geometrie-Shader kann die Datenmenge, die von einem einzelnen Aufruf ausgegeben wird, variieren. Einige Ausgaben werden vom gemeinsamen Shaderkern interpretiert (z. B. Scheitelpunktposition und Renderzielarrayindex), andere sind so konzipiert, dass sie von einer Anwendung interpretiert werden.
-   **Shadercode:** Shader können aus dem Arbeitsspeicher lesen, Vektor-Gleitkomma- und ganzzahlige arithmetische Operationen oder Flusssteuerungsvorgänge ausführen. Es gibt keine Beschränkung für die Anzahl von Anweisungen, die in einem Shader implementiert werden können.
-   **Sampler:** Sampler definieren, wie Texturen entnommen und gefiltert werden. Bis zu 16 Sampler können gleichzeitig an einen Shader gebunden werden.
-   **Texturen:** Texturen können mit Samplern gefiltert oder direkt mit der systeminternen Load-Funktion pro Texel [gelesen](dx-graphics-hlsl-to-load.md) werden.
-   **Puffer:** Puffer werden nie gefiltert, können jedoch direkt mit der systeminternen Load-Funktion pro Element aus [dem](dx-graphics-hlsl-to-load.md) Arbeitsspeicher gelesen werden. Bis zu 128 Textur- und Pufferressourcen (kombiniert) können gleichzeitig an einen Shader gebunden werden.
-   **Konstantenpuffer:** Konstante Puffer sind für Shaderkonstuntervariablen optimiert. Bis zu 16 konstante Puffer können gleichzeitig an eine Shaderphase gebunden werden. Sie sind für eine häufigere Aktualisierung der CPU konzipiert. daher gelten zusätzliche Größen-, Layout- und Zugriffseinschränkungen.


Unterschiede zwischen Direct3D 9 und Direct3D 10:

- In Direct3D 9 hatte jede Shadereinheit eine einzelne, kleine konstante Registerdatei zum Speichern aller konstanten Shadervariablen. Die Aufnahme aller Shader mit diesem begrenzten konstanten Speicherplatz erforderte eine häufige Wiederverwendung von Konstanten durch die CPU.
- In Direct3D 10 werden Konstanten in unveränderlichen Puffern im Arbeitsspeicher gespeichert und wie jede andere Ressource verwaltet. Es gibt keine Beschränkung für die Anzahl konstanter Puffer, die eine Anwendung erstellen kann. Durch das Organisieren von Konstanten in Puffern nach Aktualisierungs- und Nutzungshäufigkeit kann die Bandbreite, die zum Aktualisieren von Konstanten erforderlich ist, um alle Shader zu berücksichtigen, erheblich reduziert werden.



 

## <a name="integer-and-bitwise-support"></a>Ganzzahlige und bitweise Unterstützung

Der allgemeine Shaderkern bietet einen vollständigen Satz von IEEE-konformen 32-Bit-Ganzzahlen und bitweise Operationen. Diese Vorgänge ermöglichen eine neue Klasse von Algorithmen in Grafikhardwarebeispielen, z. B. Komprimierungs- und Packtechniken, FFTs und bitfield-Programmflusssteuerung.

Die **Datentypen int** und **uint** in Direct3D 10 HLSL sind 32-Bit-Ganzzahlen in der Hardware zuordnen.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> In Direct3D 9 wurden Streameingaben, die in HLSL als ganze Zahl gekennzeichnet sind, als Gleitkomma interpretiert. In Direct3D 10 werden als ganze Zahl markierte Streameingaben als 32-Bit-Ganzzahl interpretiert.<br/> Darüber hinaus sind boolesche Werte jetzt alle Bits festgelegt oder alle Bits nicht festgelegt. Daten, die in **bool** konvertiert werden, werden als TRUE interpretiert, wenn der Wert nicht gleich 0,0f ist (positive und negative Nullen dürfen false sein) und andernfalls FALSE.<br/> |



 

## <a name="bitwise-operators"></a>Bitweise Operatoren

Der allgemeine Shaderkern unterstützt die folgenden bitweise Operatoren:



| Operator  | Funktion          |
|-----------|-------------------|
| ~         | Logical Not       |
| <<  | Linksverschiebung        |
| >>  | Rechtsverschiebung       |
| &         | Logisches UND       |
| \|        | Logisches ODER.        |
| ^         | Logisches Xor       |
| <<= | Left shift Equal  |
| >>= | Rechtsverschiebung gleich |
| &=        | Und gleich         |
| \|=       | Oder gleich          |
| ^=        | Xor Equal         |



 

Bitweise Operatoren werden so definiert, dass sie nur für **int-** und **uint-Datentypen** verwendet werden. Der Versuch, bitweise Operatoren für **float-** oder **struct-Datentypen** zu verwenden, führt zu einem Fehler. Bitweise Operatoren haben im Hinblick auf andere Operatoren die gleiche Rangfolge wie C.

## <a name="binary-casts"></a>Binäre Casts

Die Umwandlung zwischen einer ganzen Zahl und einem Gleitkommatyp konvertiert den numerischen Wert nach C-Abschneideregeln. Die Umwandlung eines Werts von **einem float-Wert** in einen **int-Wert** und zurück in einen **float-Wert** ist eine verlustbewegte Konvertierung, die von der Genauigkeit des Zieldatentyps abhängig ist. Hier sind einige der Konvertierungsfunktionen: [**asfloat (DirectX HLSL),**](dx-graphics-hlsl-asfloat.md) [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).

Binäre Casts können auch mit systeminternen HLSL-Funktionen ausgeführt werden. Diese bewirken, dass der Compiler die Bitdarstellung einer Zahl im Zieldatentyp neu interpretiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





