---
title: Lokale Leave-Rückrufe
description: Nachdem der Multicastgruppen-Manager von IGMP benachrichtigt wurde, dass keine weiteren Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicastgruppen-Manager den PMGM \_ LOCAL \_ LEAVE \_ CALLBACK-Rückruf zum Routingprotokoll auf dieser Schnittstelle auf, sofern vorhanden. Dieser Rückruf benachrichtigt das Routingprotokoll über die Änderung.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4cd346ac3d84a5c763c7f8f866e21a1bffa2af533e5710c86ec8826ad7db45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790640"
---
# <a name="local-leave-callbacks"></a>Lokale Leave-Rückrufe

Nachdem der Multicastgruppen-Manager von IGMP benachrichtigt wurde, dass keine weiteren Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicastgruppen-Manager den [**PMGM \_ LOCAL \_ LEAVE \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) zum Routingprotokoll auf dieser Schnittstelle auf, sofern vorhanden. Dieser Rückruf benachrichtigt das Routingprotokoll über die Änderung.

Dieser Rückruf und der [**PMGM \_ LOCAL \_ JOIN \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) werden verwendet, um die Weiterleitung zwischen IGMP- und Routingprotokollen zu synchronisieren.

 

 




