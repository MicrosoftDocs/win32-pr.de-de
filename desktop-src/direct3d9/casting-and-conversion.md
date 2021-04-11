---
description: Beim Übertragen von Werten zwischen der Host Anwendung und einem Effektparameter werden die Daten erwartungsgemäß geschrieben, wenn der Quell Datentyp (in der Host Anwendung) mit dem Ziel Datentyp (im Effektparameter) übereinstimmt.
ms.assetid: 4f3ef14a-7d67-45fe-9282-541221815d1f
title: Umwandlung und Konvertierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b8ab6ec3fccd8dc57d503de18ffe1e9e321377
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126692"
---
# <a name="casting-and-conversion"></a>Umwandlung und Konvertierung

Beim Übertragen von Werten zwischen der Host Anwendung und einem Effektparameter werden die Daten erwartungsgemäß geschrieben, wenn der Quell Datentyp (in der Host Anwendung) mit dem Ziel Datentyp (im Effektparameter) übereinstimmt. Wenn sich die Datentypen unterscheiden, erfolgt eine Umwandlung, wenn die Quelldaten neu angeordnet werden, damit Sie an das Ziel angepasst werden.

Dxsas definiert die folgenden Typkonvertierungs Regeln. Dabei handelt es sich um eine übergeordnete Gruppe von Effekt-(FX) und HLSL-Typkonvertierungs Regeln. Dxsas definiert auch einige [Parameter Wert-Modifizierer](#parameter-value-modifiers) , die sich auf den Wert auswirken können, der von der Host Anwendung an einen gebundenen Parameter übertragen wird.

## <a name="type-casting"></a>Typumwandlung

In der folgenden Tabelle wird die Umwandlung aufgelistet, die bei der Übertragung eines Datentyps in einen anderen Datentyp auftritt:



| Quellentyp                                  | Zieltyp                             | Verhalten                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                                        | INT                                          | Runden in Richtung 0 (null).                                                                                                                                                                                                                                                                                                                                                                                      |
| float, int                                   | bool                                         | Werte ungleich 0-Basierend auf einem ungleich-zu-Vergleich mit 0 (int) oder 0,0 (float) werden als true angesehen. andernfalls wird der Wert als false betrachtet.                                                                                                                                                                                                                                         |
| INT                                          | float                                        |                                                                                                                                                                                                                                                                                                                                                                                                          |
| bool                                         | int, float                                   | False wird in 0 (null) konvertiert. True wird in einen konvertiert.                                                                                                                                                                                                                                                                                                                                                     |
| texture1D, texture2D, texture3D, texturecube | Struktur                                      | Die Ziel Textur wird als Quell Textur Typ behandelt.                                                                                                                                                                                                                                                                                                                                               |
| Zeichenfolge                                       | texture1D, texture2D, texture3D, texturecube | Der Zeichen folgen Wert wird als Ressourcen Adresse behandelt und auf die gleiche Weise wie die [Initialisierungs Anmerkung des Parameters](parameter-initialization-annotation.md)aufgelöst. Wenn die Ressourcen Adresse nicht aufgelöst werden kann, ist die Umwandlung ungültig, und die Host Anwendungen müssen einen Fehler zurückgeben. Wenn die Ressource ordnungsgemäß aufgelöst wird, wird der Typ des Ausdrucks als derselbe Typ wie die aufgelöste Ressource behandelt. |



 

## <a name="class-casting"></a>Klassen Umwandlung

Zusätzlich zu den oben beschriebenen Typumwandlungs Regeln definiert dxsas den Satz von Umwandlungs Regeln, die für die Konvertierung zwischen Klassentypen erforderlich sind. Spalten Matrizen (N x 1), Zeilen Matrizen (1 x N) und numerische Strukturen werden als Vektoren behandelt.

Effekt Matrix Parameter und HLSL-Matrix Variablen können definieren, ob der Wert eine Zeilen-oder Spalten hauptmatrix ist. Allerdings behandeln die DirectX-APIs [**D3DMATRIX**](d3dmatrix.md) und [**D3DXMATRIX**](d3dxmatrix.md) immer als Zeilen-Hauptversion.



| Quell Klasse | Zielklasse | Verhalten                                                                                                                                                                                                                                                                                                                                        |
|--------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Skalar       | Skalar            | Typumwandlung anwenden.                                                                                                                                                                                                                                                                                                                             |
| Skalar       | Vektor            | Repliziert den skalaren Quell Wert nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter Typumwandlung beschrieben werden, in jede Komponente des Ziel Vektors.                                                                                                                                                                             |
| Skalar       | Matrix            | Repliziert den skalaren Quell Wert nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter Typumwandlung beschrieben werden, in jede Komponente der Ziel Matrix.                                                                                                                                                                             |
| Skalar       | Object            | Ungültige Umwandlung. Host Anwendungen müssen einen Fehler zurückgeben.                                                                                                                                                                                                                                                                                           |
| Skalar       | Struktur         | Nur gültig, wenn die Zielstruktur nur numerische Elemente enthält. Wenn gültig, replizieren Sie den skalarquellwert nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter Typumwandlung beschrieben werden, in jede Komponente der Zielstruktur.                                                                                        |
| Vektor       | Skalar            | Der zielskalar empfängt den Wert der ersten Komponente des Quell Vektors nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter [Typumwandlung](#type-casting)beschrieben werden.                                                                                                                                                       |
| Vektor       | Vektor            | Ungültige Umwandlung, wenn der Ziel Vektor mehr Komponenten aufweist als der Quell Vektor. Der Ziel Vektor empfängt nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter [Typumwandlung](#type-casting)beschrieben werden, die äußersten linken Werte des Quell Vektors. Die verbleibenden ganz rechts gerichteten Komponenten des Quell Vektors gehen verloren.             |
| Vektor       | Matrix            | Ungültige Umwandlung, es sei denn, der Quell Vektor verfügt über die gleiche Anzahl von Komponenten wie die Ziel Matrix. Wenn die Umwandlung gültig ist, wird das Verhalten der Vektor-zu-Vektor-Umwandlung angewendet.                                                                                                                                                             |
| Vektor       | Object            | Ungültige Umwandlung. Host Anwendungen müssen einen Fehler zurückgeben.                                                                                                                                                                                                                                                                                           |
| Vektor       | Struktur         | Nur gültig, wenn die Zielstruktur nur numerische Elemente enthält und nicht mehr Elemente enthält, als der Quell Vektor Komponenten aufweist. Die Elemente der Zielstruktur erhalten die am weitesten links gerichteten Komponenten des Quell Vektors nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter [Typumwandlung](#type-casting)beschrieben werden.      |
| Matrix       | Skalar            | Der zielskalarwert empfängt den Wert des linken oberen Werts der Quell Matrix nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter [Typumwandlung](#type-casting)beschrieben werden.                                                                                                                                                 |
| Matrix       | Vektor            | Ungültige Umwandlung, es sei denn, die Quell Matrix verfügt über die gleiche Anzahl von Komponenten wie der Ziel Vektor. Wenn die Umwandlung gültig ist, wird das Verhalten der oben dargestellten Vektor-zu-Vektor-Umwandlung angewendet.                                                                                                                                                       |
| Matrix       | Matrix            | Ungültige Umwandlung, wenn die Ziel Matrix mehr Komponenten als die Quell Matrix aufweist. Die Ziel Matrix empfängt die obersten Links der Quell Matrix nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter [Typumwandlung](#type-casting)beschrieben werden. Die verbleibenden unteren rechten Komponenten der Quell Matrix gehen verloren. |
| Matrix       | Object            | Ungültige Umwandlung. Host Anwendungen müssen einen Fehler zurückgeben.                                                                                                                                                                                                                                                                                           |
| Matrix       | Struktur         | Die Größe der Struktur muss gleich der Größe der Matrix sein, und alle Komponenten der Struktur müssen numerisch sein.                                                                                                                                                                                                                          |
| Object       | Skalar            | Ungültige Umwandlung. Host Anwendungen müssen einen Fehler zurückgeben.                                                                                                                                                                                                                                                                                           |
| Object       | Vektor            | Ungültige Umwandlung. Host Anwendungen müssen einen Fehler zurückgeben.                                                                                                                                                                                                                                                                                           |
| Object       | Matrix            | Ungültige Umwandlung. Host Anwendungen müssen einen Fehler zurückgeben.                                                                                                                                                                                                                                                                                           |
| Object       | Object            | Gültig, wenn die Typen der Objekte identisch sind und mit dem in [Typumwandlung](#type-casting)definierten Verhalten übereinstimmen.                                                                                                                                                                                                                   |
| Struktur    | Skalar            | Gültig, wenn die Quell Struktur mindestens einen numerischen Member enthält. Der zielskalarwert empfängt den Wert des ersten numerischen Members der Quell Struktur nach dem Anwenden der Typumwandlung und des Konvertierungs Verhaltens, die unter [Typumwandlung](#type-casting)beschrieben werden.                                                                                |
| Struktur    | Vektor            | Die Quell Struktur muss mindestens die Größe des Vektors aufweisen. Die ersten Komponenten müssen in der Größe des Ziel Vektors numerisch sein.                                                                                                                                                                                                    |
| Struktur    | Matrix            | Die Quell Struktur muss mindestens die Größe des Vektors aufweisen. Die ersten Komponenten müssen in der Größe des Ziel Vektors numerisch sein.                                                                                                                                                                                                    |
| Struktur    | Struktur         | Die Zielstruktur darf nicht größer als die Quell Struktur sein. Zwischen allen jeweiligen Quell-und Ziel Komponenten muss eine gültige Umwandlung vorhanden sein.                                                                                                                                                                                       |



 

## <a name="parameter-value-modifiers"></a>Parameterwertmodifizierer

Mit parametermodifiziereranmerkungen werden einem Parameter zusätzliche Informationen hinzugefügt, damit die Daten des Parameters ordnungsgemäß interpretiert werden können. Beispielsweise muss ein Vektor möglicherweise mit normalisierten Daten ausgedrückt werden, oder es kann eine Länge in Zoll gemessen werden. Parameter Wert-modifiziereranmerkungen weisen diese zusätzlichen Informationen auf, damit Host Anwendungen Werte ordnungsgemäß transformieren können, wenn Daten in einen Effektparameter übertragen werden.

Dies sind die Parametermodifizierer:



| Parameter Wert-Modifizierer-Anmerkungen | BESCHREIBUNG                                    |
|--------------------------------------|------------------------------------------------|
| [Sasnormalize](#sasnormalize)        | Geben Sie an, ob ein Vektor normalisiert ist. |
| [Sasunits](#sasunits)                | Geben Sie die Maßeinheiten für einen Parameter an.  |



 

### <a name="sasnormalize"></a>Sasnormalize

Die sasnormalize-Anmerkung gibt an, dass der zugeordnete Parameter ein normalisierter Wert sein sollte, wenn er zugewiesen wird. Diese Anmerkung wirkt sich nur auf die Parameter float2, float3 und float4 aus.


```
string SasNormalize = "Value";
```



Dabei ist Value entweder true oder false.

Beispiel:


```
float3 UpNormal
<
  bool SasNormalize = "True";
>;
```



### <a name="sasunits"></a>Sasunits

Die Effektparameter Daten befinden sich in den folgenden Einheiten:


```
string SasUnits = "Value";
```



der Wert ist einer der folgenden Werte:



| Messungstyp     | Wert        | BESCHREIBUNG                    |
|----------------------|--------------|--------------------------------|
| Keine Einheiten             | Leere Zeichenfolge | Keine Einheiten                       |
| Entfernung             | MM           | Millimeter                    |
|                      | cm           | Zentimeter                    |
|                      | m            | Meter                         |
|                      | 6           | Kilometer                     |
| Angle                | rad          | Radians                        |
| Time                 | ms           | Millisekunden                   |
|                      | Sek.          | Sekunden                        |
|                      | Min.          | Minuten                        |
|                      | Std.           | Stunden                          |
| Lineare Geschwindigkeit      | mm/Sek.       | Millimeter pro Sekunde         |
|                      | cm/Sek.       | Zentimeter pro Sekunde         |
|                      | m/Sek.        | Zähler pro Sekunde              |
|                      | m/Stunde         | Zähler pro Stunde                |
|                      | km/Stunde        | Kilometer pro Stunde            |
| Lineare Beschleunigung  | mm/Sek. ²      | Millimeter pro Sekunde (quadratisch) |
|                      | cm/Sek. ²      | Zentimeter pro Sekunde (quadratisch) |
|                      | m/Sek. ²       | Quadrat pro Sekunde (quadratisch)      |
|                      | m/Stunde ²        | Meter pro Stunde (quadratisch)        |
|                      | km/Stunde ²       | Kilometer pro Stunde (quadratisch)    |
| Winkelgeschwindigkeit     | Rad/Sek.      | Radiane pro Sekunde             |
| Winkel Beschleunigung | Rad/Sek. ²     | Bogenmaße pro Sekunde in Quadrat     |
| Bereich                 | mm ²          | Millimeter, Quadrat            |
|                      | cm ²          | Zentimeter quadratisch            |
|                      | m²           | Quadratmeter                 |
|                      | km²          | Kilometer quadratisch             |
| Lautstärke               | mm ³          | Millimeter, cubetat              |
|                      | cm³          | Zentimeter im cubetat              |
|                      | m³           | Zähler im cubetformat                   |
|                      | km ³          | Kilometer im Bett               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Standard Anmerkungen und Semantik Referenz](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



