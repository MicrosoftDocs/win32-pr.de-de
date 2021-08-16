---
title: Verwenden der SetSearchPreference-Methode
description: Das Aufrufen der IDirectorySearch SetSearchPreference-Methode ändert die Art und Weise, wie die Suchergebnisse abgerufen und über die IDirectorySearch-Schnittstelle dargestellt werden.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI mithilfe der SetSearchPreference-Methode
- ADSI ADSI, Beispielcode C/C++ mithilfe der SetSearchPreference-Methode
- fragt ADSI mit SetSearchPreference ab.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7f40d7af4069c9b67d9cd2634f6b7f58f51aafce95af9d4f9275b0e55fc1b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637480"
---
# <a name="using-the-setsearchpreference-method"></a>Verwenden der SetSearchPreference-Methode

Der Aufruf der [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) ändert die Art und Weise, wie die Suchergebnisse abgerufen und über die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) dargestellt werden.

Die SDK-Dokumentation definiert [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) wie folgt:


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



Mehrere Einstellungen können festgelegt werden, indem ein Array als erster Parameter und die Arraygröße als zweiter Parameter übergeben wird.


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



In diesem Beispiel wird die Seitengröße auf 100 Zeilen und der Bereich auf den \_ ADS SCOPE \_ SUBTREE-Typ festgelegt. Die Einstellung für die Seitengröße bewirkt, dass der Server daten sofort an den Client zurückgibt, nachdem 100 Zeilen berechnet wurden. Die EINSTELLUNG ADS \_ SCOPE \_ SUBTREE bewirkt, dass die Suche alle Verzweigungen in der Struktur unterhalb des Punkts umfasst, ab dem die Suche ausgeführt wird.

 

 




