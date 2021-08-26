---
title: Rückrufe für lokale Joins
description: Nachdem der Multicastgruppen-Manager von IGMP benachrichtigt wurde, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicastgruppen-Manager den PMGM \_ LOCAL \_ JOIN \_ CALLBACK-Rückruf für das Routingprotokoll auf, das die Schnittstelle besitzt, sofern vorhanden.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b3464aa645a6ab110acef09f238ffca97f781a38cc6c2602a39e7c66316490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074070"
---
# <a name="local-join-callbacks"></a>Rückrufe für lokale Joins

Nachdem der Multicastgruppen-Manager von IGMP benachrichtigt wurde, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicastgruppen-Manager den [**PMGM \_ LOCAL \_ JOIN \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) für das Routingprotokoll auf, das die Schnittstelle besitzt, sofern vorhanden. Dieser Rückruf benachrichtigt das Routingprotokoll über die Änderung.

Dieser Rückruf und der [**PMGM \_ LOCAL \_ LEAVE \_ CALLBACK-Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) werden verwendet, um die Weiterleitung zwischen IGMP und Routingprotokollen zu synchronisieren.

 

 




