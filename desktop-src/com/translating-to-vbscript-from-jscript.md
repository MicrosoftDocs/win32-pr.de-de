---
title: Übersetzen in VBScript aus JScript
description: Übersetzen in VBScript aus JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036652"
---
# <a name="translating-to-vbscript-from-jscript"></a>Übersetzen in VBScript aus JScript

In VBScript lautet der **für**... **Jede** Schleife listet die Member einer Auflistung auf. in JScript ist das **für**... die in-Schleife listet die Member eines JScript-Objekts oder-Arrays **auf** . Um eine Auflistung in JScript aufzulisten, verwenden Sie ein Enumeratorobjekt.

JScript stellt das Error-Objekt bereit, das verwendet werden kann, um Fehler abzufangen und zu behandeln. Das Error-Objekt ist analog zum VBScript-Err-Objekt.

In JScript gibt es mehrere Datentypen, wie z. b. Zahlen, Zeichen folgen, boolesche Werte, Objekte und das NULL-Attribut. VBScript verwendet nur einen Datentyp ( **Variant**), der zum Darstellen von Zeichen folgen, Zahlen, booleschen Werten und so weiter subtypisiert werden kann.

In JScript können Arrays dynamisch erweitert werden, indem ein neuer Wert für die length-Eigenschaft des Arrays festgelegt wird. In VBScript können Arrays nicht vergrößert werden. Sie müssen mit der **ReDim** -Anweisung erneut dimensioniert werden.

VBScript-und JScript-Unterstützungsfunktionen. VBScript unterstützt jedoch auch Unterroutinen. Unterroutinen ähneln Funktionen, geben jedoch keinen Wert zurück.

Bei JScript wird die Groß-/Kleinschreibung beachtet. VBScript ist nicht.

JScript wird von einer Vielzahl von Webbrowsern unterstützt, einschließlich Internet Explorer und Netscape Navigator. "Netscape Navigator" unterstützt VBScript nicht.

JScript-Arrays sind keine Arrays des Variablentyp **Variant SAFEARRAY**. Ein JScript-Skript muss ein VBArray-Objekt verwenden, um auf die Varianz Variable **SAFEARRAY** zuzugreifen. VBScript-Skripts können direkt auf **Variant-SAFEARRAY**-Variablen zugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




