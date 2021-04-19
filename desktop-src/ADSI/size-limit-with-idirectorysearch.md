---
title: Größenbeschränkung mit idirector ysearch
description: Der Client kann sich auf eine kleine Anzahl von Objekten konzentrieren, die vom Server zurückgegeben werden, und den Rest des Resultsets ignorieren.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Größenbeschränkung mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Größenbeschränkung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342028"
---
# <a name="size-limit-with-idirectorysearch"></a>Größenbeschränkung mit idirector ysearch

Um die Arbeitsspeicher Anforderung oder andere Zwecke zu verringern, kann sich der Client auf eine kleine Anzahl von Objekten konzentrieren, die vom Server zurückgegeben werden, und den Rest des Resultsets ignorieren, die nicht von Interesse sind. Um dies zu erreichen, gibt der Client die Such Größenbeschränkung und andere geeignete Suchkriterien an. Wenn das Verzeichnis z. b. die Testergebnisse eines Schulbezirks speichert, können Sie die Top-zehn Studenten mit den höchsten Testergebnissen Abfragen, indem Sie eine Größenbeschränkung von zehn (10) und eine absteigende Sortierreihenfolge angeben.

Der Standardwert für die Größenbeschränkung ist nicht begrenzt. Legen Sie zum Festlegen einer Größenbeschränkung eine Suchoption für die Suchoption " **ADS \_ searchpref \_ size \_ Limit** " mit einem **\_ ganzzahligen adstype** -Wert fest, der die maximale Größe in dem an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode über gebenden [**ADS- \_ \_ infoarray**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält.

Im folgenden Codebeispiel wird gezeigt, wie die Größenbeschränkung festgelegt wird. Ein Größenlimit von NULL gibt an, dass keine Größenbeschränkung besteht.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Für Active Directory gibt die Größenbeschränkung die maximale Anzahl von Objekten an, die von der Suche zurückgegeben werden sollen. Auch für Active Directory beträgt die maximale Anzahl von Objekten, die von einer Suche zurückgegeben werden, 1000 Objekte.

 

 




