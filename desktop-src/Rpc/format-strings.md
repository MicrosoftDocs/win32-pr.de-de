---
title: Formatzeichenfolgen
description: Eine Format Zeichenfolge ist ein interpretiertes Token, das die NDR-Engine versteht. Format Zeichenfolgen werden oft als Mops bezeichnet. in dieser Dokumentation wird der Begriff "Format Zeichenfolge" verwendet.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711429"
---
# <a name="format-strings"></a>Formatzeichenfolgen

Eine Format Zeichenfolge ist ein interpretiertes Token, das die NDR-Engine versteht. Format Zeichenfolgen werden oft als Mops bezeichnet. in dieser Dokumentation wird der Begriff "Format Zeichenfolge" verwendet.

Genauer gesagt ist ein Formatzeichen ein einzelnes (atomarische) Interpretier bares Token. Jedes Formatzeichen ist ein Byte groß. Eine Format Zeichenfolge ist eine Sequenz von Formatzeichen oder Formatierungszeichen und numerischen Daten. Der Begriff Deskriptor wird auch zum Benennen allgemeiner Sequenzen verwendet. Beispielsweise ist eine Parameter Format Zeichenfolge oder ein Parameter Deskriptor eine Format Zeichenfolge, die verwendet wird, um einen Parameter einer Routine zu beschreiben.

Format Zeichen haben eindrucksvolle symbolische Namen wie FC \_ Long oder FC \_ struct. Alle von der Mittel l und der NDR-Engine verwendeten Zeichen folgen Zeichen werden in der Datei "ndrtypes. h" definiert.

## <a name="format-string-tables"></a>Zeichen folgen Tabellen formatieren

Zwei primäre Format Zeichenfolgen-Tabellen werden von der-Engine verwendet: die Format Zeichenfolgen-Tabelle des Prozedur Formats, die- **\_ \_ Klasse \_**, die die Prozedur Deskriptoren beibehält, und die typformatzeichenfolgen- **Tabelle, die \_ \_ \_** die Datentyp Deskriptoren beibehält. Der Compiler generiert beide in den hauptstub-Dateien ( \* \_ c. c, \* \_ s. c, \* \_ p. c). Die Prozedur Format-Zeichen folgen Tabelle wird größtenteils von verschiedenen Interpretern verwendet, Sie wird jedoch auch für die Puffer Konvertierung verwendet, unabhängig vom Compilermodus. Die typformatzeichenfolgen-Tabelle wird beim Aufrufen der Kern-NDR-Engine verwendet, um bestimmte Datentypen anzugeben, an denen gearbeitet werden soll.

## <a name="format-string-notation"></a>Format Zeichen folgen Notation

Die in diesem Dokument verwendete Notation befolgt allgemeine Richtlinien für die Programmier Beschreibung, wobei ein Balken ( \| ) verwendet wird, um alternative Konstrukte und eckige Klammern ( \[ \] ) anzugeben, die zum Angeben optionaler Elemente verwendet werden. Format Zeichenfolgen werden häufig zur besseren Lesbarkeit (Verantwortlichkeit) gestapelt. In diesem Dokument bezeichnet FC ein einzelnes Formatierungszeichen. Format Zeichen werden in allen Caps mithilfe ihrer eigentlichen symbolischen Namen dargestellt. Andere beliebige Felder werden durch einen Namen und eine Größe dargestellt.

Spitzen Klammern ( <> ) werden verwendet, um die Größe der Deskriptoren anzugeben. Die in der folgenden Tabelle dargestellten Konventionen werden verwendet.



| Notation     | Bedeutung                                                   |
|--------------|-----------------------------------------------------------|
| <*Nr*>  | Die Größe des Deskriptors beträgt n Bytes.                        |
| <>     | Die Größe des Deskriptors variiert.                            |
| {<>}\* | Der Deskriptor wird beliebig oft wiederholt (0, 1, 2...). |



 

Die folgenden Formatzeichen haben eine besondere Bedeutung.



| Zeichen | Bedeutung                                   |
|-----------|-------------------------------------------|
| FC- \_ Ende   | Gibt das Ende einiger Format Zeichenfolgen an. |
| FC- \_ Pad   | Nicht interpretiertes Auffüll Zeichen.              |



 

 

 




