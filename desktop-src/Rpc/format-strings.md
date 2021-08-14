---
title: Formatzeichenfolgen
description: Eine Formatzeichenfolge ist ein interpretiertes Token, das die NDR-Engine versteht. Formatzeichenfolgen werden häufig als MOPs bezeichnet. In dieser Dokumentation wird der Begriff Formatzeichenfolge verwendet.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8c14fa649e71411c5706193e83fd9a09d30f8a0c57fec411d8c34fef675ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929867"
---
# <a name="format-strings"></a>Formatzeichenfolgen

Eine Formatzeichenfolge ist ein interpretiertes Token, das die NDR-Engine versteht. Formatzeichenfolgen werden häufig als MOPs bezeichnet. In dieser Dokumentation wird der Begriff Formatzeichenfolge verwendet.

Genauer gesagt ist ein Formatzeichen ein einzelnes (atomares) interpretierbares Token. Jedes Formatzeichen hat eine Größe von einem Byte. Eine Formatzeichenfolge ist eine Sequenz von Formatzeichen oder Formatzeichen und numerischen Daten. Der Begriff Deskriptor wird auch zum Benennen allgemeiner Sequenzen verwendet. Beispielsweise ist eine Parameterformatzeichenfolge oder ein Parameterdeskriptor eine Formatzeichenfolge, die verwendet wird, um einen Parameter einer Routine zu beschreiben.

Formatzeichen weisen suggestive symbolische Namen wie FC \_ LONG oder FC \_ STRUCT auf. Alle von MIDL und der NDR-Engine verwendeten Formatzeichenfolgenzeichen werden in der Datei Ndrtypes.h definiert.

## <a name="format-string-tables"></a>Formatieren von Zeichenfolgentabellen

Die Engine verwendet zwei primäre Formatzeichenfolgentabellen: die Formatzeichenfolgentabelle der **\_ \_ Prozedur, MIDL \_ ProcFormatString,** die die Prozedurdeskriptoren beibehält, und die Typformatzeichenfolgentabelle **\_ \_ MIDL \_ TypeFormatString,** die die Datentypdeskriptoren beibehält. Der Compiler generiert beides in den Hauptstubdateien ( \* \_ c.c, \* \_ s.c, \* \_ p.c). Die Zeichenfolgentabelle im Prozedurformat wird größtenteils von verschiedenen Interpretern verwendet, aber unabhängig vom Compilermodus auch für die Pufferkonvertierung. Die Formatzeichenfolgentabelle des Typs wird verwendet, wenn die NDR-Kern-Engine aufgerufen wird, um bestimmte Datentypen anzugeben, an denen gearbeitet werden soll.

## <a name="format-string-notation"></a>Formatzeichenfolgen-Notation

Die in diesem Dokument verwendete Notation folgt allgemeinen Programmierbeschreibungsrichtlinien, wobei ein Balken ( \| ) verwendet wird, um alternative Konstrukte und eckige Klammern ( \[ \] ) anzugeben, die zum Angeben optionaler Elemente verwendet werden. Formatzeichenfolgen werden aus Gründen der Lesbarkeit (Verantwortlichkeit) häufig gestapelt. In diesem Dokument steht FC für ein einzelnes Formatzeichen. Formatzeichen werden in allen CAPS mit ihren tatsächlichen symbolischen Namen dargestellt. Andere beliebige Felder werden durch einen Namen und eine Größe dargestellt.

Spitzenklammern ( <> ) werden verwendet, um die Größe der Deskriptoren zu kennzeichnen. Die in der folgenden Tabelle gezeigten Konventionen werden verwendet.



| Notation     | Bedeutung                                                   |
|--------------|-----------------------------------------------------------|
| <*N*>  | Die Größe des Deskriptors beträgt n Bytes.                        |
| <>     | Die Größe des Deskriptors variiert.                            |
| {<>}\* | Der Deskriptor wird beliebig oft wiederholt (0,1,2 ...). |



 

Die folgenden Formatzeichen haben eine besondere Bedeutung.



| Zeichen | Bedeutung                                   |
|-----------|-------------------------------------------|
| FC \_ END   | Gibt das Ende einiger Formatzeichenfolgen an. |
| FC \_ PAD   | Nicht interpretiertes Padzeichen.              |



 

 

 




