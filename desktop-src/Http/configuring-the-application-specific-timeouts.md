---
title: Konfigurieren der anwendungsspezifischen Timeouts
description: Konfigurieren der anwendungsspezifischen Timeouts
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Konfigurieren des HTTP-Ausdrucks für anwendungsspezifische Timeouts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1cbcdb0b0796820282673c41507f6bfcc0ebd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109738"
---
# <a name="configuring-the-application-specific-timeouts"></a>Konfigurieren der anwendungsspezifischen Timeouts

Die API-weiten HTTP-Servereinstellungen gelten für alle Serversitzungen und URL-Gruppen auf dem Computer. Diese Konfigurationen können von der Anwendung überschrieben werden, indem die anwendungsspezifischen Timeoutwerte gesetzt werden. Die Serversitzungs-Timeouts überschreiben die HTTP Server-API-weiten Timeouts und gelten für alle URL-Gruppen, die unter ihnen erstellt werden. Durch das Konfigurieren der Timeouteigenschaft für eine URL-Gruppe werden die Serversitzungs-Timeouts für alle URLs in der Gruppe überschrieben.

Die Angabe von 0 (null) für einen der Timer in der [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) für eine URL-Gruppe bewirkt, dass die HTTP-Server-API auf die Serversitzungs-Timeouts zurückgesetzt wird, sofern diese vorhanden sind, oder die Standardeinstellungen der HTTP-Server-API, wenn die Serversitzungs-Timeouts nicht vorhanden sind. Wenn beispielsweise die Serverzeitüberschreitungseigenschaft in einer URL-Gruppe vorhanden ist und der **EntityBody-Timer** 0 (null) ist, wird das Serversitzungs-Timeout verwendet. Wenn die Timeouteigenschaft nicht für eine Serversitzung festgelegt ist, wird die Standardkonfiguration der HTTP-Server-API verwendet. Um einen Timer zu deaktivieren, legen Sie den Wert auf **MAXUSHORT fest,** mit Ausnahme des **MinSendRate-Timers,** der auf **MAXULONG festgelegt ist.**

Die HTTP-Server-API kann nur den anwendungsspezifischen **HeaderWait** konfigurieren, und die **IdleConnection-Timer** sind erst wirksam, nachdem die erste Anforderung empfangen wurde. Bevor die erste Anforderung empfangen wird, werden die HTTP Server-API-weiten Timeoutwerte erzwungen. Nachdem die erste Anforderung eintrifft und einer Anforderungswarteschlange zugeordnet ist, können die anwendungsspezifischen **Timer HeaderWait** und **IdleConnection** angewendet werden. Die anwendungsspezifischen Timer werden auf alle nachfolgenden Anforderungen angewendet, die in der Anforderungswarteschlange für eine Keep-Alive-Verbindung eintreffen.

Weitere Informationen zum Konfigurieren von Timern finden Sie in den Themen [Konfigurieren der URL-Gruppe](configuring-the-url-group.md) und [Konfigurieren der Serversitzung.](configuring-the-server-session.md)

 

 




