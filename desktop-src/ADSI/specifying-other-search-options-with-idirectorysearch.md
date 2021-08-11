---
title: Angeben anderer Suchoptionen mit IDirectorySearch
description: Die IDirectorySearch-Schnittstelle bietet zusätzliche Kontrolle darüber, wie die Suche mithilfe von Suchoptionen durchgeführt wird.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Angeben anderer Suchoptionen mit IDirectorySearch ADSI
- ADSI, Search, IDirectorySearch, Andere Suchoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67105d9716934c8c7d1d56193ca0cdfde5f6a4bc4c32605420513dc62700d8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178765"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Angeben anderer Suchoptionen mit IDirectorySearch

Die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) bietet zusätzliche Kontrolle darüber, wie die Suche mithilfe von Suchoptionen durchgeführt wird. Diese Suchoptionen werden festgelegt, indem sie ein Array von [**ADS \_ SEARCHPREF \_ INFO-Strukturen**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) ausfüllen und die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) aufrufen. Weitere Informationen finden Sie in den folgenden Themen:

-   [Verwenden der SetSearchPreference-Methode](using-the-setsearchpreference-method.md)
-   [Synchrone und asynchrone Suchvorgänge mit IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Paging mit IDirectorySearch](paging-with-idirectorysearch.md)
-   [Zwischenspeichern von Ergebnis mit IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Ausführen einer Attributbereichsabfrage](performing-an-attribute-scoped-query.md)
-   [Sortieren der Suchergebnisse mit IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Empfehlungssuche mit IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Größenbeschränkung mit IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Serverzeitlimit mit IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Clientzeitlimit mit IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Zurückgeben von nur Attributnamen mit IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




