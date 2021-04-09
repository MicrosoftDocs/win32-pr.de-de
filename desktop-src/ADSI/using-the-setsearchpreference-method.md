---
title: Verwenden der setsearchpreference-Methode
description: Durch Aufrufen der IDirectorySearch-Methode setsearchpreference wird die Art und Weise geändert, in der die Suchergebnisse über die IDirectorySearch-Schnittstelle abgerufen und angezeigt werden.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- Setsearchpreference ADSI, verwenden der setsearchpreference-Methode
- ADSI ADSI, Beispielcode C/C++, mit der setsearchpreference-Methode
- fragt ADSI mithilfe von setsearchpreference ab.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036292"
---
# <a name="using-the-setsearchpreference-method"></a><span data-ttu-id="34f54-106">Verwenden der setsearchpreference-Methode</span><span class="sxs-lookup"><span data-stu-id="34f54-106">Using the SetSearchPreference Method</span></span>

<span data-ttu-id="34f54-107">Durch Aufrufen der [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode wird die Art und Weise geändert, in der die Suchergebnisse über die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle abgerufen und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="34f54-107">Calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method changes the way in which the search results are obtained and presented through the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="34f54-108">Die SDK-Dokumentation definiert [**setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="34f54-108">The SDK documentation defines [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) as follows:</span></span>


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



<span data-ttu-id="34f54-109">Mehrere Einstellungen können festgelegt werden, indem Sie ein Array als ersten Parameter und die Array Größe als zweiten Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="34f54-109">Multiple preferences may be set by passing an array as the first parameter and the array size as the second parameter.</span></span>


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



<span data-ttu-id="34f54-110">In diesem Beispiel wird die Seitengröße auf 100 Zeilen und der Gültigkeitsbereich auf den \_ \_ unter Strukturtyp ADS-Bereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34f54-110">This example sets the page size to 100 rows and the scope to the ADS\_SCOPE\_SUBTREE type.</span></span> <span data-ttu-id="34f54-111">Die Einstellung für die Seitengröße bewirkt, dass der Server sofort Daten an den Client zurückgibt, nachdem 100 Zeilen berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="34f54-111">The page size setting causes the server to immediately return data to the client, after 100 rows have been calculated.</span></span> <span data-ttu-id="34f54-112">Die \_ \_ Unterstruktur Einstellung ADS-Bereich bewirkt, dass die Suche alle Verzweigungen in der Struktur unterhalb des Punkts, von dem die Suche ausgeführt wird, umfasst.</span><span class="sxs-lookup"><span data-stu-id="34f54-112">The ADS\_SCOPE\_SUBTREE setting causes the search to encompass all branches in the tree below the point from which the search is being executed.</span></span>

 

 




