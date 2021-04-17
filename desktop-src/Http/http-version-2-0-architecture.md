---
title: Architektur (http-Server-API)
description: Die Konfigurationsobjekte Server Sitzung, Anforderungs Warteschlange und URL-Gruppe ermöglichen es Anwendungen, den HTTP-Dienst zu konfigurieren.
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc7a07cb5e0439ed82421dd413aee3b6688bc0f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391405"
---
# <a name="architecture-http-server-api"></a>Architektur (http-Server-API)

Die Konfigurationsobjekte Server Sitzung, Anforderungs Warteschlange und URL-Gruppe ermöglichen es Anwendungen, den HTTP-Dienst zu konfigurieren. Die Eigenschaften, die für diese Objekte festgelegt werden, überschreiben die Standardkonfigurationen der HTTP-Server-API

-   Server Sitzung: das Konfigurationsobjekt der obersten Ebene, das Konfigurationen für alle URL-Gruppen definiert, die unter der Sitzung erstellt werden.
-   URL-Gruppe: die URL-Gruppe, die unter der Server Sitzung erstellt wurde, enthält einen Satz von URLs, die die Konfigurationen erben, die für die Server Sitzung festgelegt sind. Die Konfigurationen der URL-Gruppe überschreiben die Server Sitzungs Konfigurationen, wenn Sie von der Anwendung festgelegt werden. Die URL-Gruppe definiert einen Teil des Namespaces, der von der Anwendung überwacht wird, und konfiguriert diesen Teil des Namespaces.
-   Anforderungs Warteschlange: dieses Objekt konfiguriert Einstellungen, die für die Anforderungs Warteschlange spezifisch sind. Diese Konfigurationen werden auf alle URLs in der Gruppe angewendet, die mit der Anforderungs Warteschlange verknüpft ist.

Das folgende Diagramm zeigt die Beziehung zwischen den Konfigurationsobjekten und der Anwendung. In der Regel wird für jede Anwendung eine einzelne Server Sitzung mit einer oder mehreren jeweils erstellten URL-Gruppen erstellt. Die Anforderungs Warteschlangen werden unabhängig von der URL-Gruppe oder der Server Sitzung erstellt. URL-Gruppen müssen mit einer Anforderungs Warteschlange verknüpft werden, um Anforderungen zu empfangen.

![Beziehung zwischen den Konfigurationsobjekten und der Anwendung](images/architecture.png)

Das benannte Anforderungs Warteschlangen Feature der HTTP-Server Version 2,0-API ermöglicht es mehreren Arbeitsprozessen, Anforderungen in einer Anforderungs Warteschlange zu empfangen. Die Anforderungs Warteschlange wird von einem Controller Prozess erstellt, der die Arbeitsprozesse identifiziert, die Zugriff auf die Anforderungs Warteschlange erhalten. Weitere Informationen finden Sie im Thema " [benannte Anforderungs Warteschlange](named-request-queue.md) ".

## <a name="property-configuration"></a>Eigenschaften Konfiguration

Weitere Informationen zum Festlegen von Eigenschaften für die Konfigurationsobjekte finden Sie in den folgenden Themen:

-   [Konfigurieren der Anforderungs Warteschlange](configuring-the-request-queue.md)
-   [Konfigurieren der Server Sitzung](configuring-the-server-session.md)
-   [Konfigurieren der URL-Gruppe](configuring-the-url-group.md)

In der folgenden Tabelle werden die Eigenschaften aufgelistet, die für die Konfigurationsobjekte festgelegt sind. Weitere Informationen zu Eigenschafts Konfigurationen finden Sie im Thema [Konfigurieren von Eigenschaften in HTTP-Version 2,0](configuring-properties-in-http-version-2-0.md) .



| Name           | Eigenschaft                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server Sitzung | Httpserverstateproperty<br/> Httpserverloggingproperty<br/> Httpserverbandwidthproperty<br/> Httpservertimeoutsproperty<br/> Httpserverauthentialisionproperty<br/>                                                                               |
| URL-Gruppe      | Httpserverstateproperty<br/> Httpserverauthentialisionproperty<br/> Httpserverloggingproperty<br/> Httpserverconnectionsproperty<br/> Httpserverbandwidthproperty<br/> Httpserverbindingproperty<br/> Httpservertimeoutsproperty<br/> |
| Anforderungs-Warteschlange  | Httpserverstateproperty<br/> Httpserverqueuelengthproperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





