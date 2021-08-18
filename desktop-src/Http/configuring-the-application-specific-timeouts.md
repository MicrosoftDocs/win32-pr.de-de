---
title: Konfigurieren der anwendungsspezifischen Timeouts
description: Konfigurieren der anwendungsspezifischen Timeouts
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Konfigurieren des anwendungsspezifischen HTTP-Timeouts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722d44c1377a3bee22a88fe92f0f5aed272c08f0b0a6645361c4e03816f408fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950879"
---
# <a name="configuring-the-application-specific-timeouts"></a>Konfigurieren der anwendungsspezifischen Timeouts

Die HTTP-Server-API-weiten Einstellungen gelten für alle Serversitzungen und URL-Gruppen auf dem Computer. Diese Konfigurationen können von der Anwendung überschrieben werden, indem die anwendungsspezifischen Timeoutwerte festgelegt werden. Die Serversitzungstimeouts überschreiben die HTTP-Server-API-weiten Timeouts und gelten für alle URL-Gruppen, die darunter erstellt wurden. Durch das Konfigurieren der Timeouts-Eigenschaft für eine URL-Gruppe werden die Serversitzungstimeouts für alle URLs in der Gruppe überschrieben.

Das Angeben von 0 (null) für einen der Timer in der [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) für eine URL-Gruppe bewirkt, dass die HTTP-Server-API auf die Serversitzungstimeouts zurückgesetzt wird, sofern diese vorhanden sind, oder die Standardeinstellungen der HTTP-Server-API, wenn die Serversitzungstimeouts nicht vorhanden sind. Wenn z. B. die Servertimeouteigenschaft in einer URL-Gruppe vorhanden ist und der **EntityBody-Timer** 0 (null) ist, wird das Serversitzungstimeout verwendet. Wenn die Timeouteigenschaft in einer Serversitzung nicht festgelegt ist, wird die STANDARDkonfiguration der HTTP-Server-API verwendet. Um einen Timer zu deaktivieren, legen Sie den Wert auf **MAXUSHORT** fest, mit Ausnahme des **MinSendRate-Timers,** der auf **MAXULONG** festgelegt ist.

Die HTTP-Server-API kann nur den anwendungsspezifischen **HeaderWait** konfigurieren, und die **IdleConnection-Timer** sind erst wirksam, nachdem die erste Anforderung empfangen wurde. Bevor die erste Anforderung empfangen wird, werden die TIMEOUT-Werte für die HTTP-Server-API erzwungen. Nachdem die erste Anforderung eingetroffen ist und einer Anforderungswarteschlange zugeordnet ist, können die anwendungsspezifischen **HeaderWait-** und **IdleConnection-Timer** angewendet werden. Die anwendungsspezifischen Timer werden auf alle nachfolgenden Anforderungen angewendet, die für eine Keep-Alive-Verbindung in der Anforderungswarteschlange eingehen.

Weitere Informationen zum Konfigurieren von Timern finden Sie in den Themen [Konfigurieren der URL-Gruppe](configuring-the-url-group.md) und [Konfigurieren der Serversitzung.](configuring-the-server-session.md)

 

 




