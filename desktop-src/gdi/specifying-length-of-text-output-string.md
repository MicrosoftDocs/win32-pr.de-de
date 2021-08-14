---
description: Einige der Schriftart- und Textausgabefunktionen verfügen über einen Parameter, der die Länge der Textausgabezeichenfolge angibt. Ein typisches Beispiel ist der cchText-Parameter von DrawTextEx.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Angeben der Länge der Textausgabezeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35a673a23a310da33536f389c85a44af68b895e4f05e0a0f835656e7bc3fbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885948"
---
# <a name="specifying-length-of-text-output-string"></a>Angeben der Länge der Textausgabezeichenfolge

Einige der Schriftart- und Textausgabefunktionen verfügen über einen Parameter, der die Länge der Textausgabezeichenfolge angibt. Ein typisches Beispiel ist der *cchText-Parameter* von [**DrawTextEx.**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)

Jede dieser Funktionen verfügt sowohl über eine "ANSI"-Version als auch über eine Unicode-Version (z.B. [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) bzw. **DrawTextExW).** Für die "ANSI"-Version jeder Funktion wird die Länge als BYTE-Anzahl und für die Unicode-Funktion als WORD-Anzahl angegeben.

Es ist üblich, sich dies als "Zeichenanzahl" zu vorstellen. Dies ist in der Regel für viele Sprachen, einschließlich Englisch, aber im Allgemeinen nicht genau. In "ANSI"-Zeichenfolgen nehmen Zeichen in [SBCS-Codepages](../intl/single-byte-character-sets.md) jeweils ein Byte an, aber die meisten Zeichen auf [DBCS-Codepages](../intl/double-byte-character-sets.md) nehmen zwei Bytes an. Ebenso befinden sich die meisten derzeit definierten Unicode-Zeichen in der basic Multilingual Plane (BMP), und ihre UTF-16-Darstellungen passen in ein WORD, aber ergänzende Zeichen werden in Unicode durch "Ersatzzeichen" dargestellt, die zwei WORDs erfordern.

Jede dieser Funktionen nimmt eine Längenanzahl an. Für die "ANSI"-Version jeder Funktion wird die Länge als BYTE-Anzahllänge einer Zeichenfolge angegeben, die nicht das **NULL-Abschlusszeichen** enthält. Für die Unicode-Funktion ist die Längenanzahl die Byteanzahl dividiert durch sizeof(WCHAR), die 2 ist, ohne das **NULL-Abschlusszeichen.** Die Zeichenanzahl ist die Anzahl der Zeichen, die möglicherweise nicht der Längenanzahl der Zeichenfolge entspricht. In einigen Fällen nehmen Zeichen mehr als ein BYTE für ANSI (z. B. [DBCS-Zeichen)](../intl/double-byte-character-sets.md) und mehr als ein WORD für Unicode (z. B. Ersatzzeichen) an. Darüber hinaus entspricht die Anzahl der Glyphen möglicherweise nicht der Anzahl von Zeichen, da mehrere Zeichen zusammengesetzt werden können, um ein Glyphen zu erstellen. Längenanzahl ist die Datenmenge. Zeichenanzahl ist die Anzahl der Einheiten, die als eine Entität verarbeitet werden. Glyphen werden gerendert. In Unicode können Sie z. B. eine Zeichenfolge mit einer Länge von 3 haben, die 2 Zeichen lang ist und dazu führt, dass 1 Glyphe gerendert wird. In der Regel sind jedoch die meisten Unicode-Zeichenfolgen Länge, Zeichenanzahl und Anzahl der gerenderten Glyphen gleich.

Sie können \_ tcslen() verwenden, um die Zeichenfolgenlänge abzurufen. Für ANSI \_ gibt tcslen() die Anzahl der Bytes zurück. Für Unicode \_ gibt tcslen() die Anzahl der WCHARs (d.h. WORDs) zurück.

Spezielle Verarbeitungszeichen wie Tabstopps und weiche Bindestriche, die nicht immer gezeichnet werden, können sich auf die gezeichnete Ausgabe auswirken. Sie werden in die Zeichenfolgenlänge und die Zeichenanzahl eingeschlossen, werden aber möglicherweise nicht direkt durch ein gerenderte Glyphe dargestellt.

Einige dieser Funktionen ermöglichen es dem Aufrufer, die Länge als -1 anzugeben, um anzugeben, dass die Zeichenfolge NULL-terminiert ist. In diesem Fall berechnet die Funktion die Zeichenanzahl automatisch. Nicht alle Funktionen bieten diese Funktion. Dies wird auf Funktionsbasis angegeben. weitere Informationen finden Sie in der Dokumentation zu einzelnen Funktionen.

 

 
