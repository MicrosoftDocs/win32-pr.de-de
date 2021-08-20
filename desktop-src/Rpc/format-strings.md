---
title: Formatzeichenfolgen
description: Eine Formatzeichenfolge ist ein interpretiertes Token, das die NDR-Engine versteht. Formatzeichenfolgen werden häufig als MOPs bezeichnet. in dieser Dokumentation wird der Begriff Formatzeichenfolge verwendet.
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

Eine Formatzeichenfolge ist ein interpretiertes Token, das die NDR-Engine versteht. Formatzeichenfolgen werden häufig als MOPs bezeichnet. in dieser Dokumentation wird der Begriff Formatzeichenfolge verwendet.

Genauer gesagt ist ein Formatzeichen ein einzelnes (atomares) interpretierbares Token. Jedes Formatzeichen ist ein Byte groß. Eine Formatzeichenfolge ist eine Sequenz von Formatzeichen oder Formatzeichen und numerischen Daten. Der Begriff Deskriptor wird auch für die Benennung gängiger Sequenzen verwendet. Beispielsweise ist eine Parameterformatzeichenfolge oder ein Parameterdeskriptor eine Formatzeichenfolge, die zum Beschreiben eines Parameters einer Routine verwendet wird.

Formatzeichen haben suggestive symbolische Namen wie FC \_ LONG oder FC \_ STRUCT. Alle formatierten Zeichenfolgenzeichen, die von MIDL und der NDR-Engine verwendet werden, werden in der Datei Ndrtypes.h definiert.

## <a name="format-string-tables"></a>Formatieren von Zeichenfolgentabellen

Zwei primäre Formatzeichenfolgentabellen werden von der Engine verwendet: die Prozedurformatzeichenfolgentabelle **\_ \_ MIDL \_ ProcFormatString,** die die Prozedurdeskriptoren beibegibt, und die Typformatzeichenfolgentabelle **\_ \_ MIDL \_ TypeFormatString,** die die Datentypdeskriptoren beibegibt. Der Compiler generiert beides in den Hauptstubdateien ( \* \_ c.c, \* \_ s.c, \* \_ p.c). Die Zeichenfolgentabelle im Prozedurformat wird größtenteils von verschiedenen Interpretern verwendet, aber sie wird auch für die Pufferkonvertierung unabhängig vom Compilermodus verwendet. Die Zeichenfolgentabelle im Typformat wird beim Aufrufen der NDR-Kern-Engine verwendet, um bestimmte Datentypen anzugeben, an denen gearbeitet werden soll.

## <a name="format-string-notation"></a>Formatzeichenfolgen-Notation

Die in diesem Dokument verwendete Notation folgt allgemeinen Programmierbeschreibungsrichtlinien, mit einem Balken ( ), der verwendet wird, um alternative Konstrukte und eckige Klammern ( ) anzugeben, die zum Angeben \| \[ \] optionaler Elemente verwendet werden. Formatzeichenfolgen werden häufig gestapelt, um die Lesbarkeit (Verantwortlichkeit) zu gewährleisten. In diesem Dokument steht FC für ein einzelnes Formatzeichen. Formatzeichen werden in allen CAPS mit ihren tatsächlichen symbolischen Namen dargestellt. Andere beliebige Felder werden durch einen Namen und eine Größe dargestellt.

Eckige Klammern ( <> ) werden verwendet, um größen der Deskriptoren zu bezeichnen. Die in der folgenden Tabelle gezeigten Konventionen werden verwendet.



| Notation     | Bedeutung                                                   |
|--------------|-----------------------------------------------------------|
| <*N*>  | Die Deskriptorgröße beträgt n Bytes.                        |
| <>     | Die Deskriptorgröße variiert.                            |
| {<>}\* | Der Deskriptor wird so oft wiederholt (0,1,2 ...). |



 

Die folgenden Formatzeichen haben eine besondere Bedeutung.



| Zeichen | Bedeutung                                   |
|-----------|-------------------------------------------|
| FC \_ END   | Gibt das Ende einiger Formatzeichenfolgen an. |
| FC \_ PAD   | Nicht interpretiertes Padzeichen.              |



 

 

 




