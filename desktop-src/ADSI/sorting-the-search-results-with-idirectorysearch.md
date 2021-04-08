---
title: Sortieren der Suchergebnisse mit idirector ysearch
description: Standardmäßig werden die Ergebnisse einer Suche in einer nicht garantierten Reihenfolge zurückgegeben. Die Sortierung "ADS \_ searchpref" nach \_ \_ Belieben weist den Server an, das Resultset nach einem angegebenen Attribut Wert zu sortieren, bevor es an den Client zurückgegeben wird.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Sortieren der Suchergebnisse mit idirector ysearch
- ADSI, Search, idirector ysearch, andere Suchoptionen, Sortieren von Suchergebnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730240"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Sortieren der Suchergebnisse mit idirector ysearch

Standardmäßig werden die Ergebnisse einer Suche in einer nicht garantierten Reihenfolge zurückgegeben. Die **Sortierung "ADS \_ searchpref \_ \_** " nach Belieben weist den Server an, das Resultset nach einem angegebenen Attribut Wert zu sortieren, bevor es an den Client zurückgegeben wird.

Es wird empfohlen, dass indizierte Attribute für das Sortieren verwendet werden. Andernfalls muss der Server das gesamte Resultset abrufen und vor dem Senden von Ergebnissen an den Client sortieren. Dies gilt auch für auslagerbare Suchvorgänge. Beachten Sie, dass die Leistung einer sortierten Suche zunimmt, wenn der Filter ein indiziertes Attribut enthält und dieses Attribut als Sortierschlüssel angegeben wird. in diesem Fall können Active Directory den Sortiervorgang bei der Verarbeitung des Filters erfüllen. Eine effiziente Sortier Abfrage für eine Gruppe von Benutzern könnte z. b. über einen Filter verfügen, der (SN>Smith) und einen Sortierschlüssel von SN enthielt.

Durch die serverseitige Sortierung mit der Option " **ADS \_ searchpref \_ Sort \_ on** Search" wird die Leistung des Servers reduziert. Wenn Sie viele Suchvorgänge durchführen, sollten Sie die Ergebnisse manuell auf der Clientseite sortieren, um die Arbeitsauslastung auf dem Server zu verringern.

Die Ergebnis Sortierung ist standardmäßig deaktiviert. Legen Sie zum Aktivieren der Ergebnis Sortierung **eine ADS \_ searchpref \_ Sort \_ on** Search-Option mit einem **adstype \_ Prov- \_ spezifischen** fest, der auf eine [**ADS \_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) -Struktur im [**ADS \_ searchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Array verweist, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode weitergegeben wird. Die **ADS \_ SortKey** -Struktur wird verwendet, um das Attribut anzugeben, nach dem sortiert werden soll, und die Sortierreihenfolge.

Im folgenden Codebeispiel wird gezeigt, wie die Ergebnis Sortierung aktiviert wird.


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



Active Directory unterstützt das Sortieren nach konstruierten Attributen nicht, daher ist es nicht möglich, ein konstruiertes Attribut für die Sortierung anzugeben. Das Attribut "Unterscheidung nach [**Name**](/windows/desktop/ADSchema/a-distinguishedname) " kann auch nicht für die Sortierung verwendet werden. Active Directory auch das Sortieren nach mehr als einem Attribut nicht zulässt, daher kann die " **ADS \_ searchpref \_ Sort \_** for Search"-Struktur nur eine [**ADS- \_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) -Struktur enthalten.

 

 