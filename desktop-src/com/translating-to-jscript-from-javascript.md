---
title: Übersetzen in JScript aus JavaScript
description: Übersetzen in JScript aus JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c25276d569c5b461693a666d1bf8cf706b6896c0995972e1d2af0071c5760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129562"
---
# <a name="translating-to-jscript-from-javascript"></a>Übersetzen in JScript aus JavaScript

JScript ist größtenteils mit JavaScript kompatibel. Allerdings enthält JScript Version 5.0 einige Objekte, die derzeit nicht von JavaScript unterstützt werden, z. B. ActiveXObject, Enumerator, Error, Global und VBArray.

JScript 5.0 unterstützt die Ausnahmebehandlung durch **try**... **catch-Anweisungen.** JavaScript bietet derzeit keinen Fehlerbehandlungsmechanismus.

Bei der Arbeit mit JScript oder JavaScript gibt es einige kleine Unterschiede zwischen den Objektmodellimplementierungen, die von verschiedenen Webbrowsern unterstützt werden. Um Skripts zu schreiben, die sowohl auf Internet Explorer als auch auf Netscape Navigator ausgeführt werden, beschränken Sie die von Ihren Skripts verwendeten Funktionen auf die im World Wide Web Consortium -Standard (W3C) für HTML-Version 3.2 angegebenen Features. Weitere Informationen zu diesem Standard finden Sie unter [HTML 3.2-Referenzspezifikation.](https://www.w3.org/TR/REC-html32.html)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in JScript](translating-to-jscript.md)
</dt> </dl>

 

 




