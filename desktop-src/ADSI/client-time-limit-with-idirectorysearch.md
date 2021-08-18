---
title: Client Time Limit with IDirectorySearch
description: Ein Client kann ein Zeitlimit festlegen, damit ein Server das Resultset zurückgibt. Wenn der Server nicht innerhalb des angegebenen Zeitraums auf eine Abfrage reagiert, kann der Client die Suche abbrechen und später erneut versuchen.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Client Time Limit with IDirectorySearch
- ADSI, Suchen, IDirectorySearch, Andere Suchoptionen, Clientzeitlimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1798094a980c41de2e1902533415839020cfd690384f0e56a37bff918d4ecc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692509"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Client Time Limit with IDirectorySearch

Ein Client kann ein Zeitlimit festlegen, damit ein Server das Resultset zurückgibt. Wenn der Server nicht innerhalb des angegebenen Zeitraums auf eine Abfrage reagiert, kann der Client die Suche abbrechen und später erneut versuchen.

Die Einstellung für das Clientzeitlimit ist nützlich, wenn ein Client eine asynchrone Suche anfordert. Bei einer asynchronen Suche stellt der Client eine Anforderung und fährt dann mit anderen Aufgaben fort, während darauf gewartet wird, dass der Server die Ergebnisse zurückgibt. Es ist möglich, dass der Server offline geschaltet werden kann, ohne den Client zu benachrichtigen. In diesem Fall erhält der Client keine Benachrichtigung darüber, ob der Server die Abfrage noch verarbeitet oder nicht mehr live ist. Die Einstellung für das Clientzeitlimit gibt dem Client eine gewisse Kontrolle über Situationen wie diese.

Der Standardwert für das Clientzeitlimit ist kein Limit. Um ein Clientzeitlimit festzulegen, legen Sie eine **ADS \_ SEARCHPREF \_ TIMEOUT-Suchoption** mit einem **ADSTYPE \_ INTEGER-Wert** fest, der das Clientzeitlimit in Sekunden im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält, das an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird. Ein Clientzeitlimit von 0 (null) gibt kein Zeitlimit an.

Im folgenden Codebeispiel wird gezeigt, wie Sie das Clientzeitlimit festlegen.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




