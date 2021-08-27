---
title: Multicast-Gruppen-Manager-Rückrufe
description: Der Multicastgruppen-Manager verwendet die folgenden Rückrufe, um Clients (in der Regel Routingprotokolle) über Ereignisse und Statusänderungen zu benachrichtigen.
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037281a2cb636b337c5133c2c3a261e2c435a136a30d0ccfdcf0407a9b62509b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036650"
---
# <a name="multicast-group-manager-callbacks"></a>Multicast-Gruppen-Manager-Rückrufe

Der Multicastgruppen-Manager verwendet die folgenden Rückrufe, um Clients (in der Regel Routingprotokolle) über Ereignisse und Statusänderungen zu benachrichtigen:

[**\_ \_ PMGM-ERSTELLUNGSWARNUNGSRÜCKRUF \_**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**PMGM \_ JOIN \_ ALERT \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**PMGM \_ PRUNE \_ ALERT \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**PMGM \_ LOCAL \_ JOIN \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**PMGM \_ LOCAL \_ LEAVE \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**\_PMGM-RPF-RÜCKRUF \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**PMGM \_ WRONG \_ IF \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

Der Multicastgruppen-Manager verwendet die folgenden Rückrufe, um IGMP über Ereignisse und Zustandsänderungen zu benachrichtigen:

[**PMGM– \_ \_ IGMP-RÜCKRUF \_ DEAKTIVIEREN**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**PMGM– \_ \_ IGMP-RÜCKRUF \_ AKTIVIEREN**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 