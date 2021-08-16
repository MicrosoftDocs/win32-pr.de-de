---
title: In-Context Hookfunktionen
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: Weitere Informationen zu In-Context Hookfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbeb6340642d63700901d9306aea5dca20b26ce46790d900e26e42875571379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565561"
---
# <a name="in-context-hook-functions"></a>In-Context Hookfunktionen

In der folgenden Liste werden die wichtigsten Aspekte von Kontexthookfunktionen beschrieben:

-   Hookfunktionen im Kontext müssen sich in einer DLL (Dynamic Link Library) befinden, die das System dem Adressraum des Servers zuzuordnen hat.
-   Kontextbezogene Hookfunktionen nutzen den Adressraum gemeinsam mit dem Server.
-   Wenn der Server ein Ereignis auslöst, ruft das System eine Hookfunktion auf, ohne gemarshallt zu werden (Paketieren und Senden von Schnittstellenparametern über Prozessgrenzen hinweg).
-   Hookfunktionen im Kontext sind in der Regel sehr schnell und empfangen Ereignisbenachrichtigungen synchron, da kein Marshalling erfolgt.
-   Einige Ereignisse können außerhalb des Prozesses übermittelt werden, obwohl Sie anfordern, dass sie prozessin-process übermittelt werden (mithilfe des WINEVENT \_ INCONTEXT-Flags). Diese Situation kann bei 64-Bit- und 32-Bit-Anwendungsinteroperabilitätsproblemen und bei Windows Konsolenereignissen auftreten.

 

 




