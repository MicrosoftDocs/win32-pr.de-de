---
title: Versionierung (http-Server-API)
description: Die HTTP Server-API, Version 2,0, wendet die Versionsverwaltung auf Objektebene an, um die Version der API zu ermitteln.
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- Versionierung in der HTTP-Server Version 2,0-API
- HTTP Server, Version 2,0, API, Versionsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221ff7a93bb24e7e0b8a1b9f7c2399012cdbe95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102683"
---
# <a name="versioning-http-server-api"></a>Versionierung (http-Server-API)

Mit der HTTP-Server Version 2,0-API werden die Anforderungs Warteschlangen und die URL-Zuordnungen der Anforderungs Warteschlange in Version 1,0 Mithilfe der objektbezogenen Versionsverwaltung können Anwendungen anwendungsspezifische Versionsinformationen bereitstellen. Anwendungen können automatisch die korrekte Version der Strukturen für das Betriebssystem, auf dem Sie ausgeführt wird, abrufen.

## <a name="request-queues"></a>Anforderungs Warteschlangen

Beginnend mit der HTTP Server-API, Version 2,0, werden Anforderungs Warteschlangen mit [**httpkreaterequestqueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) erstellt, sodass die [**httpkreatehttphandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) -Funktion der Version 1,0 veraltet ist. URL-Gruppen werden mit der Funktion " [**httpkreateurlgroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) " in Version 2,0 eingeführt. URLs werden mithilfe von [**httpaddurltourlgroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) zur Gruppe hinzugefügt, wodurch die [**httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl) -Funktion der Version 1,0 veraltet ist. URL-Gruppen der Version 2,0 dürfen nicht mit Anforderungs Warteschlangen der Version 1,0 verwendet werden.

Ab Version 2,0 sind die folgenden Funktionen der Version 1,0 veraltet und können nicht mit den Anforderungs Warteschlangen der Version 2,0 verwendet werden:

-   [**Httpkreatehttphandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**Httpaddurl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**Httpremoveurl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

Weitere Informationen zum Konfigurieren von URL-Gruppen finden Sie im Thema [Konfigurieren der URL-Gruppe](configuring-the-url-group.md) . Weitere Informationen zu den Anforderungs Warteschlangen der Version 2,0 finden Sie im Thema [benannte Anforderungs Warteschlange](named-request-queue.md) .

## <a name="object-scoped-versioning"></a>Object-Scoped Versionsverwaltung

In Version 1,0 stellt die Anwendung die HTTP-Server-API-Version im [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)-Rückruf bereit. Die Versionsinformationen werden nur von der ersten Anwendung akzeptiert, die **httpinitialize** aufgerufen hat, und werden auf alle HTTP-Server-API-Anwendungen im gleichen Prozess angewendet. Beginnend mit der API der Version 2,0 werden die Informationen zur globalen Version, die im **httpinitialize** -Rückruf bereitgestellt werden, nicht verwendet. Bei Anwendungen der Version 2,0 wird die HTTP-Server-API-Version im Versions Parameter übergeben, wenn die Anforderungs Warteschlange oder die Server Sitzung von [**httpkreaterequestqueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) oder [**httpkreateserversession**](/windows/desktop/api/Http/nf-http-httpcreateserversession)erstellt wird. Wenn die Anforderungs Warteschlange mit der Version 1,0 [**httpkreatehttphandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)erstellt wird, wird Sie automatisch als Version 1,0 gekennzeichnet. Die Anwendungen Version 1,0 und Version 2,0 können in demselben Prozess ausgeführt werden.

Die [**http- \_ Anforderungs**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) -und [**http- \_ Antwort**](http-response.md) Strukturen werden so aktualisiert, dass Sie Authentifizierungsinformationen in der HTTP Server-API der Version 2,0 enthalten. [**Http \_ Die Anforderungen \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) und [**http \_ Request \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) sind spezifisch für die Version der API, die von der Anwendung verwendet wird. Anwendungen sollten diese Strukturen jedoch nicht direkt in Ihrem Code verwenden. Stattdessen sollten Sie eine **http- \_ Anforderung** verwenden, um die richtige Version basierend auf der Version der Anforderungs Warteschlange zu erhalten, für die die Anforderung empfangen wurde. Beachten Sie außerdem, dass die Größe der **http- \_ Anforderungs** Struktur auf der Version des Betriebssystems basiert, unter dem der Code kompiliert wird.

 

 
