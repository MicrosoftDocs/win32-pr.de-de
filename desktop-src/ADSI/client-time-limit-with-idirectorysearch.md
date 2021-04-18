---
title: Client Zeit Limit mit idirector ysearch
description: Ein Client kann ein Zeitlimit für einen Server erzwingen, um das Resultset zurückzugeben. Wenn der Server nicht innerhalb des angegebenen Zeitraums auf eine Abfrage reagieren kann, kann der Client die Suche verwerfen und später erneut versuchen.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Client Zeit Limit mit idirector ysearch
- ADSI, Search, idirector ysearch, andere Suchoptionen, Client Zeit Limit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339181"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Client Zeit Limit mit idirector ysearch

Ein Client kann ein Zeitlimit für einen Server erzwingen, um das Resultset zurückzugeben. Wenn der Server nicht innerhalb des angegebenen Zeitraums auf eine Abfrage reagieren kann, kann der Client die Suche verwerfen und später erneut versuchen.

Die Einstellung für das Client Zeit Limit ist nützlich, wenn ein Client eine asynchrone Suche anfordert. Bei einer asynchronen Suche sendet der Client eine Anforderung und fährt dann mit anderen Tasks fort, während er darauf wartet, dass der Server die Ergebnisse zurückgibt. Es ist möglich, dass der Server offline geschaltet werden kann, ohne den Client zu benachrichtigen. In diesem Fall wird der Client nicht benachrichtigt, ob der Server die Abfrage noch verarbeitet oder nicht mehr aktiv ist. Die Einstellung Client Zeit Limit ermöglicht dem Client eine gewisse Kontrolle über solche Situationen.

Der Standardwert für das Client Zeit Limit ist unbegrenzt. Zum Festlegen eines Client Zeitlimits legen Sie die Suchoption **ADS \_ searchpref \_ Timeout** mit einem **\_ ganzzahligen adstype** -Wert fest, der das Client Zeitlimit (in Sekunden) in der [**\_ \_ Infodatei von ADS searchpref**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält, die an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übermittelt wird. Ein Client Zeit Limit von 0 (null) gibt keine Zeitbeschränkung an.

Im folgenden Codebeispiel wird gezeigt, wie das Client Zeit Limit festgelegt wird.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




