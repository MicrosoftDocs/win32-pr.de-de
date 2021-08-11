---
title: Größenbeschränkung mit IDirectorySearch
description: Der Client kann sich auf eine kleine Anzahl von Objekten konzentrieren, die vom Server zurückgegeben werden, und den Rest des Resultset ignorieren.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Größenbeschränkung mit IDirectorySearch ADSI
- ADSI, Suchen, IDirectorySearch, Andere Suchoptionen, Größenbeschränkung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6ee4e23cb3014ea92e8510da88767a433b76c0fe73ccbe74bac6ba0bfc1c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178745"
---
# <a name="size-limit-with-idirectorysearch"></a>Größenbeschränkung mit IDirectorySearch

Um die Arbeitsspeicheranforderungen oder zu anderen Zwecken zu reduzieren, kann sich der Client auf eine kleine Anzahl von Objekten konzentrieren, die vom Server zurückgegeben werden, und den Rest des Resultset ignorieren, das nicht von Interesse ist. Um dies zu erreichen, gibt der Client die Größenbeschränkung für die Suche und andere geeignete Suchkriterien an. Wenn das Verzeichnis beispielsweise die Testergebnisse eines Schulgebiets speichert, können Sie die zehn besten Studenten mit den höchsten Testergebnissen abfragen, indem Sie eine Größenbeschränkung von zehn (10) und eine absteigende Sortierreihenfolge angeben.

Der Standardwert für das Größenlimit ist kein Limit. Legen Sie zum Festlegen eines Größenlimits die Suchoption **ADS \_ SEARCHPREF \_ SIZE \_ LIMIT** mit einem **ADSTYPE \_ INTEGER-Wert** fest, der die maximale Größe im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält, das an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird.

Das folgende Codebeispiel zeigt, wie Sie die Größenbeschränkung festlegen. Der Wert 0 (null) gibt an, dass keine Größenbeschränkung festgelegt ist.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Für Active Directory gibt die Größenbeschränkung die maximale Anzahl von Objekten an, die von der Suche zurückgegeben werden sollen. Für Active Directory beträgt die maximale Anzahl von Objekten, die von einer Suche zurückgegeben werden, 1.000 Objekte.

 

 




