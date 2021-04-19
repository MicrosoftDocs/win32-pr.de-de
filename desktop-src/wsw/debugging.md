---
title: Debuggen (Windows-Webdienste)
description: Eine Reihe von Funktionen ist nur im Debugbuild verfügbar und zum Testen und Debuggen vorgesehen.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Debuggen von Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341571"
---
# <a name="debugging-windows-web-services"></a>Debuggen (Windows-Webdienste)

Eine Reihe von Funktionen ist nur im Debugbuild verfügbar und zum Testen und Debuggen vorgesehen.


Eine Reihe von Funktionen und Umgebungsvariablen sind nur im Debugmodus verfügbar. Sie können zum Testen und Debuggen verwendet werden.

-   Durch Festlegen von wstimeout = 0 werden alle Timeouts unendlich. Dies ist nützlich, wenn der Debugger bei zeitsensiblen Vorgängen durchlaufen wird.
-   Das Festlegen von wsfailcount hat denselben Effekt wie das Aufrufen von wssetautofail.
-   Mit wsflags können Sie verschiedene Flags festlegen, die das Laufzeitverhalten ändern. Die Syntax ist wsflags = a, b, c. Die unterstützten Flags sind modifytimestamp, modifyinclusiveprefixes, modifytimestampdigest, modifyyheaderdigest und modifysignaturevalue.

Die folgenden Funktionen werden beim Debuggen verwendet:

-   [**Wsdumpmemory**](wsdumpmemory.md)
-   [**Wssetauentfail**](wssetautofail.md)

 

 




