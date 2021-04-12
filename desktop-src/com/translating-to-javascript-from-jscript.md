---
title: Übersetzen von JScript in JavaScript
description: Übersetzen von JScript in JavaScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389974"
---
# <a name="translating-to-javascript-from-jscript"></a>Übersetzen von JScript in JavaScript

JScript ist größtenteils mit JavaScript kompatibel. JScript enthält jedoch einige Objekte, die zurzeit nicht von JavaScript unterstützt werden, z. b. ActiveXObject, Enumerator, Error, Global und VBArray.

JScript-Version 5,0 unterstützt die Ausnahmebehandlung durch **try**... **catch** -Anweisungen. JavaScript stellt derzeit keinen Mechanismus zur Fehlerbehandlung bereit.

Beim Arbeiten mit JScript oder JavaScript gibt es einige feine Unterschiede zwischen den Objektmodell Implementierungen, die von verschiedenen Webbrowsern unterstützt werden. Um Skripts zu schreiben, die sowohl in Internet Explorer als auch in Netscape Navigator ausgeführt werden, schränken Sie die von Ihren Skripts verwendeten Features auf die im World Wide Web Consortium (W3C) [Standard für die HTML-Version 3,2](https://www.w3.org/tr/rec-html32.html)verwendeten Funktionen ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




