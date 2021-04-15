---
title: Übersetzen in JScript aus JavaScript
description: Übersetzen in JScript aus JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104516641"
---
# <a name="translating-to-jscript-from-javascript"></a>Übersetzen in JScript aus JavaScript

JScript ist größtenteils mit JavaScript kompatibel. Die JScript-Version 5,0 enthält jedoch einige Objekte, die zurzeit nicht von JavaScript unterstützt werden, z. b. ActiveXObject, Enumerator, Error, Global und VBArray.

JScript 5,0 unterstützt die Ausnahmebehandlung durch **try**... **catch** -Anweisungen. JavaScript stellt derzeit keinen Mechanismus zur Fehlerbehandlung bereit.

Beim Arbeiten mit JScript oder JavaScript gibt es einige feine Unterschiede zwischen den Objektmodell Implementierungen, die von verschiedenen Webbrowsern unterstützt werden. Um Skripts zu schreiben, die sowohl in Internet Explorer als auch in Netscape Navigator ausgeführt werden, schränken Sie die von Ihren Skripts verwendeten Features auf die im World Wide Web Consortium (W3C) Standard für die HTML-Version 3,2 verwendeten Funktionen ein. Weitere Informationen zu diesem Standard finden Sie unter [HTML 3,2 Reference Specification](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in JScript](translating-to-jscript.md)
</dt> </dl>

 

 




