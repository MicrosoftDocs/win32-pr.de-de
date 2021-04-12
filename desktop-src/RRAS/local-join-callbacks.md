---
title: Lokale joinrückrufe
description: Nachdem der Multicast-Gruppen-Manager von IGMP benachrichtigt wurde, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicast-Gruppen-Manager den pmgm- \_ \_ Rückruf Rückruf \_ Rückruf auf das Routing Protokoll auf, der die Schnittstelle besitzt, sofern vorhanden.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471549"
---
# <a name="local-join-callbacks"></a>Lokale joinrückrufe

Nachdem der Multicast-Gruppen-Manager von IGMP benachrichtigt wurde, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicast-Gruppen-Manager den [**pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) Rückruf Rückruf auf das Routing Protokoll auf, der die Schnittstelle besitzt, sofern vorhanden. Dieser Rückruf benachrichtigt das Routing Protokoll über die Änderung.

Dieser Rückruf und der [**lokale pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) Rückruf werden verwendet, um die Weiterleitung zwischen IGMP und Routing Protokollen zu synchronisieren.

 

 




