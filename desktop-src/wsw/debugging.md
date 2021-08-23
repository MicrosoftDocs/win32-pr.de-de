---
title: Debuggen (Windows Webdienste)
description: Ein Satz von Funktionen ist nur im DEBUG-Build verfügbar und dient zum Testen und Debuggen.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Debuggen von Webdiensten für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135f81ec45028df098679c91d750915005bfc64b3ff7d072b0494badc98159fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838680"
---
# <a name="debugging-windows-web-services"></a>Debuggen (Windows Webdienste)

Ein Satz von Funktionen ist nur im DEBUG-Build verfügbar und dient zum Testen und Debuggen.


Es gibt eine Reihe von Funktionen und Umgebungsvariablen, die nur im DEBUG-Modus verfügbar sind. Sie können zum Testen und Debuggen verwendet werden.

-   Das Festlegen von WsTimeout=0 verursacht, dass alle Timeouts INFINITE sind. Dies ist nützlich, wenn Sie den Debugger während zeitsensibler Vorgänge durchschritten.
-   Das Festlegen von WsFailCount hat die gleiche Auswirkung wie das Aufrufen von WsSetAutoFail.
-   Mit WsFlags können Sie verschiedene Flags festlegen, die das Laufzeitverhalten ändern. Die Syntax ist WsFlags=a,b,c. Die unterstützten Flags sind ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest und ModifySignatureValue.

Die folgenden Funktionen werden beim Debuggen verwendet:

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




