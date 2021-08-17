---
title: Server Time Limit with IDirectorySearch
description: Um zu vermeiden, dass die gesamte CPU-Zeit verwendet wird und andere Vorgänge nicht ausgeführt werden, geben Sie das Suchzeitlimit auf einen kleinen Wert an, und führen Sie die Anwendung später erneut aus, wenn der Bericht nicht generiert werden kann.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Server Time Limit with IDirectorySearch ADSI
- ADSI, Suchen, IDirectorySearch, Andere Suchoptionen, Serverzeitlimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e120586cb05fa07baf1e26fa8c1db8e11eecdbd1b19ed7f4f9c2215a921409ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262130"
---
# <a name="server-time-limit-with-idirectorysearch"></a>Server Time Limit with IDirectorySearch

Wenn Sie eine Suche auf einem ausgelasteten Server anfordern, können Sie anfordern, dass der Server die Suche auf ein angegebenes Zeitlimit beschränkt. Beispielsweise möchten Sie eine Anwendung ausführen, um einen wöchentlichen Bericht auf einem Server zu generieren, der in der Nähe seiner Kapazität ausgeführt wird. Um zu vermeiden, dass die gesamte CPU-Zeit verwendet wird und andere Vorgänge nicht ausgeführt werden, geben Sie das Suchzeitlimit auf einen kleinen Wert an, und führen Sie die Anwendung später erneut aus, wenn der Bericht nicht generiert werden kann.

Einige Server legen möglicherweise ein eigenes Administratives Zeitlimit fest. Wenn Sie in diesen Fällen einen Suchzeitlimitwert angeben, der größer als das administrative Zeitlimit ist, ignoriert der Server Ihre Spezifikation und verwendet stattdessen den internen Zeitlimitwert.

Die Standardeinstellung für das Serverzeitlimit ist kein Limit. Um ein Serverzeitlimit festzulegen, legen Sie eine **ADS \_ SEARCHPREF \_ TIME \_ LIMIT-Suchoption** mit einem **ADSTYPE \_ INTEGER-Wert** fest, der das Serverzeitlimit in Sekunden im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält, das an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird. Dieser Vorgang wird im folgenden Codebeispiel gezeigt. Ein Serverzeitlimit von 0 (null) gibt kein Zeitlimit an.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




