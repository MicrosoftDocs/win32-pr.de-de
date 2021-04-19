---
description: Wspeventselect verhält sich genau wie wspasyncselect, mit dem Unterschied, dass anstelle einer Windows-Meldung nach dem Auftreten eines beliebigen nominierten FD \_ xxx-Netzwerk Ereignisses (z. b \_ . FD Read, FD \_ Write usw.) ein bestimmtes Ereignis Objekt festgelegt wird.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Ereignis Objekt Signalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346941"
---
# <a name="event-object-signaling"></a>Ereignis Objekt Signalisierung

[**Wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) verhält sich genau wie [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , mit dem Unterschied, dass anstelle einer Windows-Meldung nach dem Auftreten eines beliebigen nominierten FD \_ xxx-Netzwerk Ereignisses (z. b. FD \_ Read, FD \_ Write usw.) ein bestimmtes Ereignis Objekt festgelegt wird.

Außerdem wird der Dienstanbieter daran erinnert, dass ein bestimmtes FD \_ xxx-Netzwerk Ereignis aufgetreten ist. Dies ist erforderlich, da das Vorkommen eines und aller nominierten Netzwerkereignisse dazu führt, dass ein einzelnes Ereignis Objekt signalisiert wird. Ein Aufruf von [**wspenumnetworkevents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) bewirkt, dass der aktuelle Inhalt des Netzwerk Ereignis Speichers in einen vom Client bereitgestellten Puffer kopiert und der Netzwerk Ereignisspeicher gelöscht wird. Der Client kann auch ein bestimmtes Ereignis Objekt festlegen, das atomisch zusammen mit dem Netzwerk Ereignisspeicher gelöscht werden soll.

 

 
