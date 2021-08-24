---
title: Arbeiten mit den nächsten Hops
description: Mit der RTMv2-API können Clients mit der Liste der nächsten Hops arbeiten, die Routen und Zielen zugeordnet sind.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f629bb5f43298c2cada3759ea3ab9c7bb71f0ca47a3c4158028d923646662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024710"
---
# <a name="working-with-next-hops"></a>Arbeiten mit den nächsten Hops

Mit der RTMv2-API können Clients mit der Liste der nächsten Hops arbeiten, die Routen und Zielen zugeordnet sind. Clients können einen nächsten Hop hinzufügen oder aktualisieren, indem [**sie RtmAddNextHop aufrufen.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop) Clients können einen nächsten Hop mit [**rtmDeleteNextHop löschen.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop) Clients können nach nächsten Hops suchen, indem [**sie RtmFindNextHop aufrufen.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)

Clients können den nächsten Hop auch direkt aktualisieren. Dazu muss der Client zuerst den nächsten Hop mit der [**RtmLockNextHop-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) sperren. Anschließend kann der Client den direkten Zeiger auf die [**RTM \_ NEXTHOP \_ INFO-Struktur**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) des Routingtabellen-Managers verwenden, um erforderliche Änderungen zu nehmen. Schließlich kann der Client den nächsten Hop entsperren.

> [!Note]  
> Die Felder für die Adresse des nächsten Hops und den Schnittstellenindex im nächsten Hop identifizieren den nächsten Hop eindeutig und sollten nicht geändert werden.

 

 

 




