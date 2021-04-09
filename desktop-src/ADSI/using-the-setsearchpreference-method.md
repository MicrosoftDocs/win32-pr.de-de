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
# <a name="using-the-setsearchpreference-method"></a>Verwenden der setsearchpreference-Methode

Durch Aufrufen der [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode wird die Art und Weise geändert, in der die Suchergebnisse über die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle abgerufen und angezeigt werden.

Die SDK-Dokumentation definiert [**setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) wie folgt:


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



Mehrere Einstellungen können festgelegt werden, indem Sie ein Array als ersten Parameter und die Array Größe als zweiten Parameter übergeben.


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



In diesem Beispiel wird die Seitengröße auf 100 Zeilen und der Gültigkeitsbereich auf den \_ \_ unter Strukturtyp ADS-Bereich festgelegt. Die Einstellung für die Seitengröße bewirkt, dass der Server sofort Daten an den Client zurückgibt, nachdem 100 Zeilen berechnet wurden. Die \_ \_ Unterstruktur Einstellung ADS-Bereich bewirkt, dass die Suche alle Verzweigungen in der Struktur unterhalb des Punkts, von dem die Suche ausgeführt wird, umfasst.

 

 




