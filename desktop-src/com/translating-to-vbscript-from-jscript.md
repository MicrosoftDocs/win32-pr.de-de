---
title: Übersetzen von JScript in VBScript
description: Übersetzen von JScript in VBScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3900ba82b258e6ee19cf06edb2f97247033778da5fcabaffe4a854e66a5fef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992250"
---
# <a name="translating-to-vbscript-from-jscript"></a>Übersetzen von JScript in VBScript

In VBScript wird **für**... **Jede** Schleife listet die Member einer Auflistung auf. in JScript **für**... **in-Schleife** listet die Member eines JScript Objekts oder Arrays auf. Um eine Auflistung in JScript aufzuzählen, verwenden Sie ein Enumeratorobjekt.

JScript stellt das Error-Objekt bereit, das zum Abfangen und Behandeln von Fehlern verwendet werden kann. Das Error-Objekt entspricht dem VBScript Err-Objekt.

In JScript gibt es mehrere Datentypen wie Zahlen, Zeichenfolgen, Boolesche Werte, Objekte und das NULL-Attribut. VBScript verwendet nur einen Datentyp, **Variant**, der subtypisiert werden kann, um Zeichenfolgen, Zahlen, Boolesche Werte usw. darzustellen.

In JScript können Arrays dynamisch erweitert werden, indem ein neuer Wert für die length-Eigenschaft des Arrays festgelegt wird. In VBScript können Arrays nicht vergrößert werden. Sie müssen mithilfe der **redim-Anweisung** neu dimensioniert werden.

Sowohl VBScript als auch JScript unterstützen Funktionen. VBScript unterstützt jedoch auch Unterroutinen. Unterroutinen ähneln Funktionen, geben jedoch keinen Wert zurück.

JScript wird die Groß-/Kleinschreibung beachtet. VBScript ist dies nicht.

JScript wird von einer Vielzahl von Webbrowsern unterstützt, einschließlich Internet Explorer und Netscape Navigator. Netscape Navigator unterstützt VBScript nicht.

JScript Arrays sind keine Arrays des Variablentyps **VARIANT SAFEARRAY**. Ein JScript Skript muss ein VBArray-Objekt verwenden, um auf die **VARIANT SAFEARRAY-Variable** zuzugreifen. VBScript-Skripts können direkt auf **VARIANT SAFEARRAY-Variablen** zugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




