---
title: Übersetzen von VBScript in JScript
description: Übersetzen von VBScript in JScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708033"
---
# <a name="translating-to-jscript-from-vbscript"></a>Übersetzen von VBScript in JScript

In VBScript lautet der **für**... **Jede** Schleife listet die Member einer Auflistung auf. in JScript ist das **für**... die in-Schleife listet die Member eines JScript-Objekts oder-Arrays **auf** . Um eine Auflistung in JScript aufzulisten, verwenden Sie ein Enumeratorobjekt.

In JScript gibt es mehrere Datentypen, wie z. b. Zahlen, Zeichen folgen, boolesche Werte, Objekte und das NULL-Attribut. VBScript verwendet nur einen Datentyp ( **Variant**), der zum Darstellen von Zeichen folgen, Zahlen, booleschen Werten und so weiter subtypisiert werden kann.

In JScript können Arrays dynamisch erweitert werden, indem ein neuer Wert für die length-Eigenschaft des Arrays festgelegt wird. In VBScript können Arrays nicht vergrößert werden. Sie müssen mit der **ReDim** -Anweisung erneut dimensioniert werden.

VBScript-und JScript-Unterstützungsfunktionen. VBScript unterstützt jedoch auch Unterroutinen. Unterroutinen ähneln Funktionen, geben jedoch keinen Wert zurück.

Bei JScript wird die Groß-/Kleinschreibung beachtet. VBScript ist nicht.

JScript wird sowohl von Internet Explorer als auch von Netscape Navigator unterstützt. "Netscape Navigator" unterstützt VBScript nicht.

JScript stellt das Error-Objekt bereit, das verwendet werden kann, um Fehler abzufangen und zu behandeln. Das Error-Objekt ist analog zum VBScript-Err-Objekt.

JScript-Arrays sind keine Arrays des Variablentyp **Variant SAFEARRAY**. Wenn Ihr Skript eine Varianz **-Varianz Variable von** einem COM-Objekt oder einem VBScript-Skript empfängt, muss es ein VBArray-Objekt verwenden, um auf die Varianz Variable **SAFEARRAY** zuzugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in JScript](translating-to-jscript.md)
</dt> </dl>

 

 




