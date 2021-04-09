---
title: Multicast-Gruppen-Manager-Rückrufe
description: Der Multicast-Gruppen-Manager verwendet die folgenden Rückrufe, um Clients (in der Regel Routing Protokolle) von Ereignissen und Statusänderungen zu benachrichtigen.
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858363"
---
# <a name="multicast-group-manager-callbacks"></a>Multicast-Gruppen-Manager-Rückrufe

Der Multicast-Gruppen-Manager verwendet die folgenden Rückrufe, um Clients (in der Regel Routing Protokolle) von Ereignissen und Statusänderungen zu benachrichtigen:

[**pmgm-Warnungs \_ \_ \_ Rückruf**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**pmgm- \_ Join- \_ Benachrichtigungs \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**pmgm- \_ \_ Benachrichtigungs \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**pmgm \_ , \_ lokaler \_ joinrückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**lokaler pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**pmgm- \_ RPF- \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**pmgm \_ falsch, \_ Wenn \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

Der Multicast-Gruppen-Manager verwendet die folgenden Rückrufe, um IGMP über Ereignisse und Statusänderungen zu benachrichtigen:

[**pmgm \_ deaktiviert \_ IGMP- \_ Rückruf**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**pmgm \_ enable \_ IGMP- \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 