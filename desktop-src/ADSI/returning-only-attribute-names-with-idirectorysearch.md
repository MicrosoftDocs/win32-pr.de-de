---
title: Zurückgeben von nur Attributnamen mit IDirectorySearch
description: Sie können eine Suche durchführen, um zu bestimmen, welcher Datentyp für ein bestimmtes Objekt verfügbar ist.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Zurückgeben von nur Attributnamen mit IDirectorySearch ADSI
- ADSI, Suchen, IDirectorySearch, andere Suchoptionen, Zurückgeben von nur Attributnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b9c69a99cad0ece5c660ba45954fe537abe69cfa88947b52b0d69d7833b4e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444010"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Zurückgeben von nur Attributnamen mit IDirectorySearch

Sie können eine Suche durchführen, um zu bestimmen, welcher Datentyp für ein bestimmtes Objekt verfügbar ist. In diesem Fall sind sie nur an den Attributnamen interessiert, nicht an den Attributwerten des Objekts. Die **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY-Option** bewirkt, dass der Server nur die Attributnamen und nicht die Attributwerte zurück gibt. Das Ergebnisset enthält jedoch nur die Attribute, denen Werte zugewiesen sind. Betrachten Sie beispielsweise ein Objekt mit den folgenden Attributen:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Wenn die **OPTION ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** festgelegt ist, enthält das Resultset Folgendes:

``` syntax
name
sn
department
phone
```

Der Standardwert ist, dass sowohl Attributwerte als auch Namen zurückgegeben werden.

Um nur Attributnamen abzurufen, legen Sie eine **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY-Suchoption** mit dem **ADSTYPE \_ BOOLEAN-Wert** **TRUE** im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) fest, das an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird.

Das folgende Codebeispiel zeigt, wie nur Attributnamen abgerufen werden.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Weitere Informationen und ein Codebeispiel, das zeigt, wie die **SUCHoption ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** verwendet wird, finden Sie unter Beispielcode für die Suche [nach Attributen.](example-code-for-searching-for-attributes.md)

 

 




