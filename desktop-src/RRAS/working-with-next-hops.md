---
title: Arbeiten mit den nächsten Hops
description: Mit der RTMv2-API können Clients mit der Liste der nächsten Hops arbeiten, die Routen und Zielen zugeordnet sind.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388679"
---
# <a name="working-with-next-hops"></a>Arbeiten mit den nächsten Hops

Mit der RTMv2-API können Clients mit der Liste der nächsten Hops arbeiten, die Routen und Zielen zugeordnet sind. Clients können einen nächsten Hop durch Aufrufen von [**rtmaddnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)hinzufügen oder aktualisieren. Clients können einen nächsten Hop mit [**rtmdeletenexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)löschen. Clients können durch Aufrufen von [**rtmfindnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)nach den nächsten Hops suchen.

Clients können den nächsten Hop auch direkt aktualisieren. Zu diesem Zweck muss der Client zunächst den nächsten Hop mit der Funktion [**rtmlocknexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) sperren. Anschließend kann der Client den direkten Zeiger zur [**RTM \_ nexthop- \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) Struktur des Routing Tabellen-Managers verwenden, um die erforderlichen Änderungen vorzunehmen. Schließlich kann der Client den nächsten Hop entsperren.

> [!Note]  
> Die Felder "Address" und "Interface Index" im nächsten Hop identifizieren den nächsten Hop eindeutig und sollten nicht geändert werden.

 

 

 




