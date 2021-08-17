---
description: WSPEventSelect verhält sich genau wie WSPAsyncSelect, außer dass ein bestimmtes Ereignisobjekt festgelegt wird, anstatt zu bewirken, dass eine Windows-Nachricht beim Auftreten eines beliebigen FD XXX-Netzwerkereignisses (z. B. \_ FD \_ READ, FD \_ WRITE usw.) gesendet wird.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Ereignisobjektsignalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eed237db696298a2f8053fb61cb0009d9d25d7f37497e0a19d58044d27d8dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132622"
---
# <a name="event-object-signaling"></a>Ereignisobjektsignalisierung

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) verhält sich genau wie [**WSPAsyncSelect,**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) außer dass ein bestimmtes Ereignisobjekt festgelegt wird, anstatt zu bewirken, dass eine Windows-Nachricht beim Auftreten eines beliebigen FD XXX-Netzwerkereignisses (z. B. \_ FD \_ READ, FD \_ WRITE usw.) gesendet wird.

Darüber hinaus wird die Tatsache, dass ein bestimmtes \_ FD XXX-Netzwerkereignis aufgetreten ist, vom Dienstanbieter gespeichert. Dies ist erforderlich, da das Auftreten von allen einheitlichen Netzwerkereignissen dazu führt, dass ein einzelnes Ereignisobjekt signalisiert wird. Ein Aufruf von [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) bewirkt, dass der aktuelle Inhalt des Netzwerkereignisspeichers in einen vom Client bereitgestellten Puffer kopiert und der Netzwerkereignisspeicher entlastet wird. Der Client kann auch ein bestimmtes Ereignisobjekt festlegen, das atomisch zusammen mit dem Netzwerkereignisspeicher ent cleared werden soll.

 

 
