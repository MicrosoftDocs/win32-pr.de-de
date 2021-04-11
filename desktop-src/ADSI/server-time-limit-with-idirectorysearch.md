---
title: Server Zeit Limit bei idirector ysearch
description: Um zu vermeiden, dass die gesamte CPU-Zeit verwendet und andere Vorgänge nicht ausgeführt werden, geben Sie das Such Zeitlimit auf einen kleinen Wert an, und führen Sie die Anwendung dann später erneut aus, wenn der Bericht nicht generiert werden kann.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Server Zeit Limit mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Server Zeit Limit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947328"
---
# <a name="server-time-limit-with-idirectorysearch"></a>Server Zeit Limit bei idirector ysearch

Wenn Sie eine Suche auf einem ausgelasteten Server anfordern, möchten Sie möglicherweise anfordern, dass der Server die Suche auf ein angegebenes Zeitlimit beschränkt. Sie möchten z. b. eine Anwendung ausführen, um einen wöchentlichen Bericht auf einem Server zu generieren, der in der Nähe seiner Kapazität ausgeführt wird. Um zu vermeiden, dass die gesamte CPU-Zeit verwendet und andere Vorgänge nicht ausgeführt werden, geben Sie das Such Zeitlimit auf einen kleinen Wert an, und führen Sie die Anwendung dann später erneut aus, wenn der Bericht nicht generiert werden kann.

Einige Server erzwingen möglicherweise eine eigene administrative Zeitbegrenzung. Wenn Sie in diesen Fällen einen Wert für das Such Zeitlimit angeben, der größer ist als das administrative Zeit Limit, ignoriert der Server Ihre Spezifikation und verwendet stattdessen den internen Wert des Zeitlimits.

Der Standardwert für das Serverzeit Limit ist unbegrenzt. Zum Festlegen eines Serverzeit Limits legen Sie eine Suchoption für die Suchoption " **ADS \_ searchpref \_ time \_ Limit** " mit einem **\_ ganzzahligen adstype** -Wert fest, der das Server Zeitlimit (in Sekunden) in dem an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode über gebenden [**ADS \_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält. Dieser Vorgang wird im folgenden Codebeispiel gezeigt. Ein Serverzeit Limit von 0 (null) gibt an, dass kein Zeit Limit


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




