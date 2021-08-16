---
title: VML Eqn-Attribut
description: VML Eqn-Attribut
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae5872c29064f24a10b4a12c0d0e2a4ca4a200f79e295d60713fe56355f23aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655450"
---
# <a name="vml-eqn-attribute"></a>VML Eqn-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die von einer Formel verwendete Gleichung. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[F](msdn-online-vml-f-element.md) (Unterelement von [Formeln](msdn-online-vml-formulas-element.md))

**Tagsyntax**

<v: *element* eqn="-Ausdruck "> 

**Skriptsyntax**

*element* .eqn="*expression*"

*expression* = *Element*.eqn

**Anmerkungen**

Gleichungen werden durch die Auswertung eines Textausdrucks definiert, der die allgemeine Form eines Vorgangs hat, gefolgt von bis zu drei Argumenten. Jedes Argument kann die folgenden Typen haben:

-   Anpassung (z. B. \# 2)
-   eine andere Formel (z. B. @2 )
-   Feste Zahlen (z. B. 2)
-   Vordefinierte Werte

In der folgenden Tabelle werden die Formeln definiert, die mit den optionalen Argumenten unter den Namen *v,* *p1* und *p2 verwendet werden können.* Das Formelmuster ist:

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Vorgang | Parameter | Exact  | Ergebnis                    | BESCHREIBUNG                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| Val       | 1      | ja    | v                         | Definiert einen Leitfadenwert aus einem anderen Wert.                                   |
| Sum       | 3      | ja    | v + p1 - p2               | Wird für Addition und Subtraktion verwendet.                                             |
| product   | 3      | Runden | v \* p1/p2              | Wird für Multiplikation und Division verwendet.                                          |
| mId       | 2      | (c)    | (v + p1)/ 2               | Average.                                                                       |
| abs       | 1      | ja    | abs(v)                    | Absoluter Wert.                                                                |
| Min       | 2      | ja    | min(v,p1)                 | Der geringere Wert von v und p1.                                                  |
| max       | 2      | ja    | max(v,p1)                 | Der höhere Wert von v und p1.                                                 |
| if        | 3      | ja    | v > 0 ? p1 : p2        | Bedingte Tests.                                                           |
| mod       | 3      | nein     | sqrt(v^2 + p1^2 + p2^2)   | Moduluswert.                                                                 |
| atan2     | 2      | nein     | atan2(p1,v)               | Polarwert in Grad \* 2^16 (FD-Einheiten).                                     |
| sin       | 2      | nein     | v \* sin(p1)              | Sin, Argument in Grad \* 2^16 [](msdn-online-vml-units.md) (FD-Einheiten ).     |
| cos       | 2      | nein     | v \* cos(p1)              | Cos, Argument in Grad \* 2^16 [](msdn-online-vml-units.md) (FD-Einheiten ).     |
| cosatan2  | 3      | nein     | v \* cos(atan2(p2,p1))    | Behält die vollständige Genauigkeit bei der Zwischenberechnung bei.                           |
| sinatan2  | 3      | nein     | v \* sin(atan2(p2,p1))    | Behält die vollständige Genauigkeit bei der Zwischenberechnung bei.                           |
| sqrt      | 1      | nein     | sqrt(v)                   | Das Ergebnis ist positiv und rundet ab.                                            |
| sumangle  | 3      | ja    | v + p1 \* 2^16 + p2 \* 2^16 | v skaliert um 2^16; p1 und p2 sind Grad.<br/>                            |
| ellipse   | 3      | nein     | p2 \* sqrt(1-(v/p1)^2)    | Ellipse.                                                                       |
| tan       | 2      | nein     | v \* tan(p1)              | Tangens, Argument in Grad \* 2^16 [](msdn-online-vml-units.md) (FD-Einheiten ). |



 

Beachten Sie, dass die Gleichung nur aus Vorgängen und Zahlen besteht. mathematische Symbole werden ausgelassen. Beispiel: die Gleichung

eqn="sum 5 9 3"

würde das Äquivalent von ergeben.

5 + 9 - 3

für den zurückgegebenen Wert 11. Wenn Operanden fehlen, wird der Wert nicht verwendet. Beispiel:

eqn="sum 5 9"

würde das Äquivalent von ergeben.

5 + 9

und würden den fehlenden Operanden ignorieren.

*VML-Standardattribut*

**Beispiel**

Die folgende Formel würde ein Ergebnis von 6 ergeben (die Summe beider Zahlen dividiert durch 2), was, wenn dies die erste Formel wäre, durch das Symbol " " abgerufen werden @0 kann.


```HTML
    <v:f eqn="mid 5 7"/>
```



 

