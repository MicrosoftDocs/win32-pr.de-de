---
description: Einige der Schriftart-und Textausgabe Funktionen verfügen über einen Parameter, der die Länge der Textausgabe Zeichenfolge angibt. Ein typisches Beispiel ist der cchtext-Parameter von drawtextex.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Angeben der Länge der Textausgabe Zeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c120026d1b65170b6fe35bc65400280f6f1ffa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960519"
---
# <a name="specifying-length-of-text-output-string"></a>Angeben der Länge der Textausgabe Zeichenfolge

Einige der Schriftart-und Textausgabe Funktionen verfügen über einen Parameter, der die Länge der Textausgabe Zeichenfolge angibt. Ein typisches Beispiel ist der *cchtext* -Parameter von [**drawtextex**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa).

Jede dieser Funktionen verfügt sowohl über eine ANSI-Version als auch über eine Unicode-Version (z. b. [**drawtextexa**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) bzw. **drawtextexw**). Für die ANSI-Version der einzelnen Funktionen wird die Länge als Byte Anzahl angegeben, und für die Unicode-Funktion wird Sie als Wort Anzahl angegeben.

Es ist traditionell, dies als "Zeichen Anzahl" zu betrachten. Das ist für viele Sprachen, einschließlich Englisch, im allgemeinen genau, aber im Allgemeinen ist es nicht richtig. In ANSI-Zeichen folgen verwenden Zeichen in [SBCS](../intl/single-byte-character-sets.md) -Codepages jeweils ein Byte, aber die meisten Zeichen in [DBCS](../intl/double-byte-character-sets.md) -Codepages nehmen zwei Bytes in Anspruch. Entsprechend befinden sich die meisten aktuell definierten Unicode-Zeichen in der grundlegenden multidimensionalen Ebene (BMP), und die UTF-16-Darstellungen sind in ein Wort passen, aber ergänzende Zeichen werden in Unicode durch ' ' Surrogates ' ' dargestellt, für die zwei Wörter erforderlich sind.

Jede dieser Funktionen nimmt eine Längen Anzahl an. Für die ANSI-Version der einzelnen Funktionen wird die Länge als Byte Anzahl Länge einer Zeichenfolge angegeben, die nicht das **null** -Terminator einschließt. Bei der Unicode-Funktion ist die Längen Anzahl die Byte Anzahl dividiert durch sizeof (WChar), d. h. 2, ohne das **null** -Terminator. Die Zeichen Anzahl ist die Anzahl der Zeichen, die möglicherweise nicht der Länge der Zeichenfolge entspricht. In einigen Fällen übernehmen Zeichen mehr als ein Byte für ANSI (z. b. [DBCS](../intl/double-byte-character-sets.md) -Zeichen) und mehr als ein Wort für Unicode (z. b. Ersatz Zeichen). Außerdem ist die Anzahl der Symbole möglicherweise nicht gleich der Anzahl der Zeichen, da mehrere Zeichen zusammengesetzt werden können, um ein Symbol zu erstellen. Die Längen Anzahl ist die Datenmenge. Die Zeichen Anzahl ist die Anzahl der Einheiten, die als eine Entität verarbeitet werden. Symbole werden gerendert. In Unicode können Sie z. b. eine Zeichenfolge mit einer Länge von 3 (2 Zeichen) haben, und dies führt dazu, dass 1 Symbol gerendert wird. In der Regel sind jedoch die meisten Unicode-Zeichen folgen Länge, Zeichen Anzahl und Anzahl gerenderter Symbole gleich.

Sie können \_ tcslen () verwenden, um die Länge der Zeichenfolge zu erhalten. Für ANSI \_ gibt tcslen () die Anzahl von Bytes zurück. Bei Unicode \_ gibt tcslen () die Anzahl der WCHARs (d. h. Wörter) zurück.

Spezielle Verarbeitungs Zeichen wie Registerkarten und weiche Bindestriche, die nicht immer gezeichnet werden, können sich auf die gezeichnete Ausgabe auswirken. Sie werden in die Zeichen folgen Länge und Zeichen Anzahl eingeschlossen, werden jedoch möglicherweise nicht direkt durch ein gerendertes Symbol dargestellt.

Einige dieser Funktionen ermöglichen es dem Aufrufer, die Länge als-1 anzugeben, um anzugeben, dass die Zeichenfolge NULL-terminiert ist. in diesem Fall berechnet die Funktion die Zeichen Anzahl automatisch. Nicht alle Funktionen bieten diese Funktion. , Der für Funktionsweise angegeben wird. Weitere Informationen finden Sie in der einzelnen Funktions Dokumentation.

 

 
