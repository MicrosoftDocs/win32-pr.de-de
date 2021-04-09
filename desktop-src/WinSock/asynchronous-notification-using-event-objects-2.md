---
description: Die Funktionen WSAEventSelect und WSAEnumNetworkEvents werden bereitgestellt, um Anwendungen wie Daemons und Dienste zu unterstützen, die keine Benutzeroberfläche haben (und daher keine Windows-Handles verwenden).
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: Asynchrone Benachrichtigung mit Ereignis Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862591"
---
# <a name="asynchronous-notification-using-event-objects"></a>Asynchrone Benachrichtigung mit Ereignis Objekten

Die Funktionen [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) und [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) werden bereitgestellt, um Anwendungen wie Daemons und Dienste zu unterstützen, die keine Benutzeroberfläche haben (und daher keine Windows-Handles verwenden). Die **WSAEventSelect** -Funktion verhält sich genau wie die [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -Funktion. Anstatt zu bewirken, dass eine Windows-Meldung für das Vorkommen eines FD \_ xxx-Netzwerk Ereignisses gesendet wird (z. b \_ . FD Read und FD \_ Write), wird ein Anwendungs bestimmtes Ereignis Objekt festgelegt.

Außerdem wird der Dienstanbieter daran erinnert, dass ein bestimmtes FD \_ xxx-Netzwerk Ereignis aufgetreten ist. Die Anwendung kann [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) aufzurufen, damit der aktuelle Inhalt des Netzwerk Ereignis Speichers in einen von der Anwendung bereitgestellten Puffer kopiert und der Netzwerk Ereignisspeicher automatisch gelöscht wird. Bei Bedarf kann die Anwendung auch ein bestimmtes Ereignis Objekt festlegen, das zusammen mit dem Netzwerk Ereignisspeicher gelöscht wird.

 

 



