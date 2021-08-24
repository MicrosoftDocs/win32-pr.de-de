---
title: Sortieren der Suchergebnisse mit IDirectorySearch
description: Standardmäßig werden die Ergebnisse einer Suche in keiner garantierten Reihenfolge zurückgegeben. Die ADS \_ SEARCHPREF \_ SORT \_ ON-Einstellung weist den Server an, das Resultset nach einem angegebenen Attributwert zu sortieren, bevor es an den Client zurückgegeben wird.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Sortieren der Suchergebnisse mit IDirectorySearch
- ADSI, Suchen, IDirectorySearch, Andere Suchoptionen, Sortieren von Suchergebnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7864a3878d2cdc44d58c6f6090f6b791b9fe29b3d2613e6e3d4aaf0b6289e100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443870"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Sortieren der Suchergebnisse mit IDirectorySearch

Standardmäßig werden die Ergebnisse einer Suche in keiner garantierten Reihenfolge zurückgegeben. Die **ADS \_ SEARCHPREF \_ SORT \_ ON-Einstellung** weist den Server an, das Resultset nach einem angegebenen Attributwert zu sortieren, bevor es an den Client zurückgegeben wird.

Es wird empfohlen, indizierte Attribute zum Sortieren zu verwenden. Andernfalls muss der Server das vollständige Resultset abrufen und sortieren, bevor Ergebnisse an den Client gesendet werden. Dies gilt auch für ausgelagerungte Suchvorgänge. Beachten Sie, dass die Leistung einer sortierten Suche erhöht wird, wenn der Filter ein indiziertes Attribut enthält und dieses Attribut als Sortierschlüssel angegeben wird. In diesem Fall kann Active Directory die Sortierung während der Verarbeitung des Filters erfüllen. Eine effiziente Sortierabfrage für eine Gruppe von Benutzern könnte beispielsweise einen Filter enthalten (sn>smith) und einen Sortierschlüssel von sn enthalten.

Die serverseitige Sortierung mit der Suchoption **ADS \_ SEARCHPREF \_ SORT \_ ON** verringert die Leistung des Servers. Wenn Sie viele Suchvorgänge durchführen, sollten Sie die Ergebnisse manuell auf der Clientseite sortieren, um die Arbeitsauslastung auf dem Server zu reduzieren.

Standardmäßig ist die Ergebnissortierung deaktiviert. Legen Sie zum Aktivieren der Ergebnissortierung eine **ADS \_ SEARCHPREF \_ SORT \_ ON-Suchoption** mit einem **ADSTYPE \_ PROV \_ SPECIFIC** fest, das auf eine [**ADS \_ SORTKEY-Struktur**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) verweist, die an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird. Die **ADS \_ SORTKEY-Struktur** wird verwendet, um das zu sortierende Attribut und die Sortierreihenfolge anzugeben.

Das folgende Codebeispiel zeigt, wie die Ergebnissortierung aktiviert wird.


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



Active Directory unterstützt keine Sortierung nach konstruierten Attributen, sodass es nicht möglich ist, ein konstruiertes Attribut für die Sortierung anzugeben. Das [**DistinguishedName-Attribut**](/windows/desktop/ADSchema/a-distinguishedname) kann auch nicht zum Sortieren verwendet werden. Active Directory lässt auch keine Sortierung nach mehreren Attributen zu, sodass die Suchoption **ADS \_ SEARCHPREF \_ SORT \_ ON** nur eine [**ADS \_ SORTKEY-Struktur**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) enthalten kann.

 

 