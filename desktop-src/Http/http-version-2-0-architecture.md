---
title: Architektur (HTTP-Server-API)
description: Mit den Konfigurationsobjekten Serversitzung, Anforderungswarteschlange und URL-Gruppe können Anwendungen den HTTP-Dienst konfigurieren.
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3905a27708c87c43e141dd4cf8d84b2f0e7e66bc4dd189440733321ee951a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997105"
---
# <a name="architecture-http-server-api"></a>Architektur (HTTP-Server-API)

Mit den Konfigurationsobjekten Serversitzung, Anforderungswarteschlange und URL-Gruppe können Anwendungen den HTTP-Dienst konfigurieren. Die für diese Objekte festgelegten Eigenschaften überschreiben die HTTP Server-API-weit verfügbaren Standardkonfigurationen.

-   Serversitzung: Das Konfigurationsobjekt der obersten Ebene, das Konfigurationen für alle URL-Gruppen definiert, die in der Sitzung erstellt werden.
-   URL-Gruppe: Die URL-Gruppe, die unter der Serversitzung erstellt wurde, enthält eine Reihe von URLs, die die in der Serversitzung festgelegten Konfigurationen erben. Die URL-Gruppenkonfigurationen überschreiben die Serversitzungskonfigurationen, wenn sie von der Anwendung festgelegt werden. Die URL-Gruppe definiert einen Teil des Namespace, den die Anwendung abhört, und konfiguriert diesen Teil des Namespace.
-   Anforderungswarteschlange: Dieses Objekt konfiguriert spezifische Einstellungen für die Anforderungswarteschlange. Diese Konfigurationen werden auf alle URLs in den Gruppen angewendet, die der Anforderungswarteschlange zugeordnet sind.

Das folgende Diagramm zeigt die Beziehung zwischen den Konfigurationsobjekten und der Anwendung. In der Regel wird für jede Anwendung eine einzelne Serversitzung mit mindestens einer URL-Gruppe erstellt, die darunter erstellt wird. Die Anforderungswarteschlangen werden unabhängig von der URL-Gruppe oder Serversitzung erstellt. URL-Gruppen müssen einer Anforderungswarteschlange zugeordnet werden, um Anforderungen zu empfangen.

![Beziehung zwischen den Konfigurationsobjekten und der Anwendung](images/architecture.png)

Das Feature "Benannte Anforderungswarteschlange" der HTTP Server-API version 2.0 ermöglicht es mehreren Workerprozessen, Anforderungen in einer Anforderungswarteschlange zu empfangen. Die Anforderungswarteschlange wird von einem Controllerprozess erstellt, der die Workerprozesse identifiziert, denen Zugriff auf die Anforderungswarteschlange gewährt wurde. Weitere Informationen finden Sie im Thema [Benannte Anforderungswarteschlange.](named-request-queue.md)

## <a name="property-configuration"></a>Eigenschaftenkonfiguration

Weitere Informationen zum Festlegen von Eigenschaften für die Konfigurationsobjekte finden Sie in den folgenden Themen:

-   [Konfigurieren der Anforderungswarteschlange](configuring-the-request-queue.md)
-   [Konfigurieren der Serversitzung](configuring-the-server-session.md)
-   [Konfigurieren der URL-Gruppe](configuring-the-url-group.md)

In der folgenden Tabelle sind die Eigenschaften aufgeführt, die für die Konfigurationsobjekte festgelegt sind. Weitere Informationen zu Eigenschaftenkonfigurationen finden Sie im Thema [Konfigurieren von Eigenschaften in HTTP Version 2.0.](configuring-properties-in-http-version-2-0.md)



| Name           | Eigenschaft                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serversitzung | HttpServerStateProperty<br/> HttpServerLoggingProperty<br/> HttpServerBandwidthProperty<br/> HttpServerTimeoutsProperty<br/> HttpServerAuthenticatonProperty<br/>                                                                               |
| URL-Gruppe      | HttpServerStateProperty<br/> HttpServerAuthenticatonProperty<br/> HttpServerLoggingProperty<br/> HttpServerConnectionsProperty<br/> HttpServerBandwidthProperty<br/> HttpServerBindingProperty<br/> HttpServerTimeoutsProperty<br/> |
| Anforderungs-Warteschlange  | HttpServerStateProperty<br/> HttpServerQueueLengthProperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





