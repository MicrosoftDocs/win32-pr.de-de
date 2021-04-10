---
title: Konfigurieren der anwendungsspezifischen Timeouts
description: .
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Konfigurieren der anwendungsspezifischen Timeouts http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35827b797ad6c9f19b728064f6fe65b0d89b2a3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036901"
---
# <a name="configuring-the-application-specific-timeouts"></a>Konfigurieren der anwendungsspezifischen Timeouts

Die HTTP-Server-API-weiten Einstellungen gelten für alle Server Sitzungen und URL-Gruppen auf dem Computer. Diese Konfigurationen können von der Anwendung überschrieben werden, indem die anwendungsspezifischen Timeout Werte festgelegt werden. Die Timeouts der Server Sitzung überschreiben die API-weiten Timeouts für die HTTP-Server und gelten für alle unter Ihnen erstellten URL-Gruppen. Wenn Sie die Timeouts-Eigenschaft für eine URL-Gruppe konfigurieren, werden die Timeouts der Server Sitzung für alle URLs in der Gruppe überschrieben.

Das Angeben von NULL für einen der Timer in der [**Informationsstruktur http- \_ Timeout \_ Limit \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) für eine URL-Gruppe bewirkt, dass die HTTP-Server-API die Timeout Werte der Server Sitzung wiederherstellt, wenn Sie vorhanden sind, oder die Standardeinstellungen der HTTP-Server-API, wenn die Server Sitzungs Timeouts nicht vorhanden sind. Wenn z. b. die Server Timeout-Eigenschaft in einer URL-Gruppe vorhanden ist und der **entityBody** -Timer 0 (null) ist, wird das Timeout der Server Sitzung verwendet. Wenn die Eigenschaft Timeouts für eine Server Sitzung nicht festgelegt ist, wird die Standardkonfiguration der HTTP-Server-API verwendet. Um einen Timer zu deaktivieren, legen Sie den Wert auf **maxushort** fest, mit Ausnahme des **minsendrate** -Timers, der auf **MAXULONG** festgelegt ist.

Von der HTTP-Server-API können nur die anwendungsspezifischen **Header Wait** und die **idleconnection** -Timer nur wirksam werden, nachdem die erste Anforderung empfangen wurde. Bevor die erste Anforderung empfangen wird, werden die HTTP-Server-API-weiten Timeout Werte erzwungen. Nachdem die erste Anforderung eingeht und einer Anforderungs Warteschlange zugeordnet ist, können die anwendungsspezifischen **Header Wait** und **idleconnection** angewendet werden. Die anwendungsspezifischen Timer werden auf alle nachfolgenden Anforderungen angewendet, die für eine Keep-Alive-Verbindung in der Anforderungs Warteschlange eintreffen.

Weitere Informationen zum Konfigurieren von Timern finden Sie in den Themen [Konfigurieren der URL-Gruppe](configuring-the-url-group.md) und [Konfigurieren der Server Sitzung](configuring-the-server-session.md) .

 

 




