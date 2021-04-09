---
title: IGMP-Rückrufe aktivieren und deaktivieren
description: Der Multicast-Gruppen-Manager verwendet zwei Rückrufe zu IGMP, um Änderungen im Schnittstellen Besitz von IGMP zu einem Routing Protokoll und von einem Routing Protokoll an IGMP zu koordinieren.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858404"
---
# <a name="igmp-enable-and-disable-callbacks"></a>IGMP-Rückrufe aktivieren und deaktivieren

Der Multicast-Gruppen-Manager verwendet zwei Rückrufe zu IGMP, um Änderungen im Schnittstellen Besitz von IGMP zu einem Routing Protokoll und von einem Routing Protokoll an IGMP zu koordinieren. Die Rückrufe ermöglichen es IGMP, auf einer Schnittstelle mit einem anderen Routing Protokoll (z. b. DVMRP) nebeneinander zu existieren.

Nachdem sich der Besitz einer Schnittstelle geändert hat, ruft der Multicast-Gruppen-Manager zunächst den [**pmgm-Rückruf Rückruf " \_ \_ IGMP \_ Deaktivieren**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) " auf. IGMP muss das Hinzufügen und Löschen von Gruppenmitgliedschaften auf der angegebenen Schnittstelle verhindern, bis der Multicast-Gruppen-Manager den [**pmgm-Rückruf Rückruf " \_ enable \_ IGMP \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) " aufruft.

Der Multicast-Gruppen-Manager ruft den [**pmgm- \_ Rückruf " \_ IGMP- \_ Rückruf aktivieren**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) " auf, nachdem die Änderung des Schnittstellen Besitzes beendet wurde.

 

 