---
title: VML-eqn-Attribut
description: VML-eqn-Attribut
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da00084a825147c6f8a05f503e5ee2679f40e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316413"
---
# <a name="vml-eqn-attribute"></a>VML-eqn-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Gleichung, die von einer Formel verwendet wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[F](msdn-online-vml-f-element.md) (Unterelement von [Formeln](msdn-online-vml-formulas-element.md))

**Tagsyntax**

<v: *Element* eqn = " *Expression* " >

**Skript Syntax**

*Element* . eqn = "*Ausdruck*"

*Ausdruck* = *Element*. eqn

**Anmerkungen**

Gleichungen werden durch die Auswertung eines Text Ausdrucks definiert, der über die allgemeine Form eines Vorgangs gefolgt von bis zu drei Argumenten verfügt. Jedes Argument kann die folgenden Typen aufweisen:

-   Anpassung (z. b. \# 2)
-   eine andere Formel (z. b. @2 )
-   fixierte Zahlen (z. b. 2)
-   vordefinierte Werte

In der folgenden Tabelle sind die Formeln definiert, die mit den optionalen Argumenten für die Namen " *v*", " *P1*" und " *P2*" verwendet werden können. Das Formel Muster ist:

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Vorgang | Parameter | Exact  | Ergebnis                    | BESCHREIBUNG                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| ster       | 1      | ja    | v                         | Definiert einen Führungs Wert aus einem anderen Wert.                                   |
| Sum       | 3      | ja    | v + P1-P2               | Wird für Addition und Subtraktion verwendet.                                             |
| product   | 3      | rundet | v \* P1/P2              | Wird für Multiplikation und Division verwendet.                                          |
| mId       | 2      | scher    | (v + P1)/2               | Average.                                                                       |
| abs       | 1      | ja    | Abs (v)                    | Absoluter Wert.                                                                |
| Min.       | 2      | ja    | min (v, P1)                 | Der geringere Wert von "v" und "P1".                                                  |
| max       | 2      | ja    | Max (v, P1)                 | Der höhere Wert von "v" und "P1".                                                 |
| if        | 3      | ja    | v > 0? P1: P2        | Bedingte Tests.                                                           |
| mod       | 3      | nein     | SQRT (v ^ 2 + P1 ^ 2 + P2 ^ 2)   | Modulus-Wert.                                                                 |
| atan2     | 2      | nein     | atan2 (P1, v)               | Polar Wert in Grad \* 2 ^ 16 (FD-Einheiten).                                     |
| sin       | 2      | nein     | v \* Sin (P1)              | Sin, Argument in Grad \* 2 ^ 16 (FD- [Einheiten](msdn-online-vml-units.md) ).     |
| cos       | 2      | nein     | v \* cos (P1)              | COS, Argument in Grad \* 2 ^ 16 (FD- [Einheiten](msdn-online-vml-units.md) ).     |
| cosatan2  | 3      | nein     | v \* cos (atan2 (P2, P1))    | Behält die vollständige Genauigkeit in der zwischen Berechnung bei.                           |
| sinatan2  | 3      | nein     | v \* Sin (atan2 (P2, P1))    | Behält die vollständige Genauigkeit in der zwischen Berechnung bei.                           |
| sqrt      | 1      | nein     | SQRT (v)                   | Das Ergebnis ist positiv und wird abgerundet.                                            |
| sumangle  | 3      | ja    | v + P1 \* 2 ^ 16 + P2 \* 2 ^ 16 | v skaliert um 2 ^ 16; P1 und P2 sind Grad.<br/>                            |
| ellipse   | 3      | nein     | P2 \* sqrt (1-(v/P1) ^ 2)    | Ellipse.                                                                       |
| tan       | 2      | nein     | v \* Tan (P1)              | Tangens, Argument in Grad \* 2 ^ 16 (FD- [Einheiten](msdn-online-vml-units.md) ). |



 

Beachten Sie, dass die Gleichung nur aus Vorgängen und Zahlen besteht. mathematische Symbole werden ausgelassen. Beispielsweise die Gleichung

eqn = "Sum 5 9 3"

ergibt die Entsprechung von

5 + 9-3

für den zurückgegebenen Wert 11. Wenn keine Operanden vorhanden sind, wird der Wert nicht verwendet. Beispiel:

eqn = "Sum 5 9"

ergibt die Entsprechung von

5 + 9

und würden den fehlenden Operanden ignorieren.

*VML-Standard Attribut*

**Beispiel**

Die folgende Formel ergibt ein Ergebnis von 6 (die Summe beider Zahlen dividiert durch 2), was, wenn dies die erste Formel war, durch das Symbol "" abgerufen werden konnte @0 .


```HTML
    <v:f eqn="mid 5 7"/>
```



 

