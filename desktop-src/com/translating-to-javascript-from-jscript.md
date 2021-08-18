---
title: Übersetzen von JScript in JavaScript
description: Übersetzen von JScript in JavaScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c4adb5827952cc9bab0dac268997b5b73a52ecd1403e5431cdb3939b08c7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129582"
---
# <a name="translating-to-javascript-from-jscript"></a>Übersetzen von JScript in JavaScript

JScript ist größtenteils mit JavaScript kompatibel. JScript enthält jedoch einige Objekte, die derzeit nicht von JavaScript unterstützt werden, z. B. ActiveXObject, Enumerator, Error, Global und VBArray.

JScript Version 5.0 unterstützt die Ausnahmebehandlung über **try**... **catch-Anweisungen.** JavaScript bietet derzeit keinen Fehlerhandingmechanismus.

Bei der Arbeit mit JScript oder JavaScript gibt es einige geringfügige Unterschiede zwischen den Objektmodellimplementierungen, die von verschiedenen Webbrowsern unterstützt werden. Um Skripts zu schreiben, die sowohl auf Internet Explorer als auch auf Netscape Navigator ausgeführt werden, beschränken Sie die von Ihren Skripts verwendeten Funktionen auf die im W3C-Standard (World Wide Web Consortium) [für HTML-Version 3.2](https://www.w3.org/tr/rec-html32.html)angegebenen Features.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




