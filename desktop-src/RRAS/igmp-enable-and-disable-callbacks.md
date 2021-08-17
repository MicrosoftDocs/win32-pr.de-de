---
title: 'IGMP: Aktivieren und Deaktivieren von Rückrufen'
description: Der Multicastgruppenleiter verwendet zwei Rückrufe an IGMP, um Änderungen im Schnittstellenbesitz von IGMP zu einem Routingprotokoll und von einem Routingprotokoll an IGMP zu koordinieren.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103a0f9abb4d2a78b2b87fde3cb5832b4e88eb2677851d9fe703e5162263642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791143"
---
# <a name="igmp-enable-and-disable-callbacks"></a>IGMP: Aktivieren und Deaktivieren von Rückrufen

Der Multicastgruppenleiter verwendet zwei Rückrufe an IGMP, um Änderungen im Schnittstellenbesitz von IGMP zu einem Routingprotokoll und von einem Routingprotokoll an IGMP zu koordinieren. Die Rückrufe ermöglichen igmp das gleichzeitige Verwenden einer Schnittstelle mit einem anderen Routingprotokoll, z. B. DVMRP.

Nachdem sich der Besitz einer Schnittstelle geändert hat, ruft der Multicastgruppen-Manager zuerst den [**PMGM \_ DISABLE \_ IGMP \_ CALLBACK-Rückruf**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) auf. IGMP muss das Hinzufügen und Löschen von Gruppenmitgliedschaften auf der angegebenen Schnittstelle beenden, bis der Multicastgruppen-Manager den [**PMGM \_ ENABLE \_ IGMP \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) aufruft.

Der Multicastgruppen-Manager ruft den [**PMGM \_ ENABLE \_ IGMP \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) auf, nachdem die Änderung des Schnittstellenbesitzes abgeschlossen ist.

 

 