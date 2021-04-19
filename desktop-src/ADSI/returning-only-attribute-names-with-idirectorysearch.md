---
title: Zurückgeben von Attributnamen mit idirector ysearch
description: Sie können eine Suche durchführen, um zu ermitteln, welche Art von Daten für ein bestimmtes Objekt verfügbar ist.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Zurückgeben von Attributnamen mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, zurückgeben von Attributnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341417"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Zurückgeben von Attributnamen mit idirector ysearch

Sie können eine Suche durchführen, um zu ermitteln, welche Art von Daten für ein bestimmtes Objekt verfügbar ist. In diesem Fall sind Sie nur an den Namen der Attribute interessiert, nicht an den Attributwerten des Objekts. Die Option **ADS \_ searchpref \_ attribtypes \_ only** bewirkt, dass der Server nur die Attributnamen und nicht die Attributwerte zurückgibt. Das Resultset enthält jedoch nur die Attribute, denen Werte zugewiesen sind. Nehmen Sie beispielsweise ein Objekt mit den folgenden Attributen:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Wenn die Option **ADS \_ searchpref \_ attribtypes \_ only** festgelegt ist, enthält das Resultset Folgendes:

``` syntax
name
sn
department
phone
```

Der Standardwert ist für Attributwerte und Namen, die zurückgegeben werden sollen.

Wenn Sie nur Attributnamen abrufen möchten, legen Sie die Suchoption **ADS \_ searchpref \_ attribtypes \_ only** mit dem **\_ booleschen adstype** -Wert " **true** " im [**ADS \_ searchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Array fest, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übermittelt wird.

Im folgenden Codebeispiel wird gezeigt, wie nur Attributnamen abgerufen werden.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie die Suchoption **ADS \_ searchpref \_ attribtypes \_ only** verwenden, finden Sie unter [Beispielcode für die Suche nach Attributen](example-code-for-searching-for-attributes.md).

 

 




