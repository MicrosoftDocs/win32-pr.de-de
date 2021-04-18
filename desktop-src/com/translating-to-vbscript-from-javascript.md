---
title: Übersetzen in VBScript aus JavaScript
description: Übersetzen in VBScript aus JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338169"
---
# <a name="translating-to-vbscript-from-javascript"></a>Übersetzen in VBScript aus JavaScript

In JavaScript gibt es mehrere Datentypen, z. b. Zahlen, Zeichen folgen, boolesche Werte, Objekte und das NULL-Attribut. VBScript verwendet nur einen Datentyp ( **Variant**), der zum Darstellen von Zeichen folgen, Zahlen, booleschen Werten und so weiter subtypisiert werden kann.

In JavaScript können Arrays dynamisch erweitert werden, indem ein neuer Wert für die length-Eigenschaft des Arrays festgelegt wird. In VBScript können Arrays nicht vergrößert werden. Sie müssen mit der **ReDim** -Anweisung erneut dimensioniert werden.

VBScript-und JavaScript-Unterstützungsfunktionen. VBScript unterstützt jedoch auch Unterroutinen. Unterroutinen ähneln Funktionen, mit dem Unterschied, dass Sie keinen Wert zurückgeben.

In JavaScript muss die Groß-/Kleinschreibung beachtet werden. VBScript ist nicht.

JavaScript wird von einer Vielzahl von Webbrowsern unterstützt, einschließlich Internet Explorer und Netscape Navigator. "Netscape Navigator" unterstützt VBScript nicht.

VBScript unterstützt die Fehlerbehandlung durch das Err-Objekt. JavaScript bietet derzeit keine Möglichkeit zum Abfangen und behandeln von Fehlern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




