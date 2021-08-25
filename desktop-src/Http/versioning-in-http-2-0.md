---
title: Versionierung (HTTP-Server-API)
description: Die HTTP Server Version 2.0-API wendet die objektbezogene Versionierung an, um die Version der API zu bestimmen.
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- Versionsinformationen in der HTTP Server Version 2.0-API
- HTTP Server Version 2.0 API, Versionierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc7a84af7de439cdd13cc1e9ff66fff367370fa963882077904ad656b856511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829690"
---
# <a name="versioning-http-server-api"></a>Versionierung (HTTP-Server-API)

Die HTTP Server Version 2.0-API macht die Anforderungswarteschlangen und URL-Zuordnungen der Version 1.0 mit der Anforderungswarteschlange veraltet. Mit der objektbezogenen Versionsangabe können Anwendungen anwendungsspezifische Versionsinformationen bereitstellen. Anwendungen können automatisch die richtige Version der Strukturen für das Betriebssystem aufrufen, unter dem sie ausgeführt wird.

## <a name="request-queues"></a>Anforderungswarteschlangen

Ab http Server Version 2.0 API werden Anforderungswarteschlangen mit [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) erstellt, wodurch die [**HttpCreateHttpHandle-Funktion**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) der Version 1.0 veraltet ist. URL-Gruppen werden in Version 2.0 mit der [**HttpCreateUrlGroup-Funktion**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) eingeführt. URLs werden der Gruppe mit [**httpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) hinzugefügt, wodurch die [**HttpAddUrl-Funktion**](/windows/desktop/api/Http/nf-http-httpaddurl) der Version 1.0 veraltet ist. URL-Gruppen der Version 2.0 dürfen nicht mit Anforderungswarteschlangen der Version 1.0 verwendet werden.

Ab Version 2.0 sind die folgenden Funktionen der Version 1.0 veraltet und können nicht mit Anforderungswarteschlangen der Version 2.0 verwendet werden:

-   [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

Weitere Informationen zum Konfigurieren von URL-Gruppen finden Sie im Thema [Konfigurieren der URL-Gruppe.](configuring-the-url-group.md) Weitere Informationen zu Anforderungswarteschlangen der Version 2.0 finden Sie im Thema [Benannte Anforderungswarteschlange.](named-request-queue.md)

## <a name="object-scoped-versioning"></a>Object-Scoped Versionierung

In Version 1.0 stellt die Anwendung die HTTP-Server-API-Version im Aufruf von [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)bereit. Die Versionsinformationen werden nur von der ersten Anwendung akzeptiert, die **HttpInitialize** aufgerufen hat, und werden auf alle HTTP-Server-API-Anwendungen im selben Prozess angewendet. Ab version 2.0 API werden die globalen Versionsinformationen, die im Aufruf von **HttpInitialize** bereitgestellt werden, nicht verwendet. Bei Anwendungen der Version 2.0 wird die HTTP-Server-API-Version im Version-Parameter übergeben, wenn die Anforderungswarteschlange oder Serversitzung von [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) oder [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession)erstellt wird. Wenn die Anforderungswarteschlange mit der Version 1.0 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)erstellt wird, wird sie automatisch als Version 1.0 markiert. Anwendungen der Versionen 1.0 und 2.0 können im gleichen Prozess ausgeführt werden.

Die [**HTTP \_ REQUEST-**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) und [**HTTP \_ RESPONSE-Strukturen**](http-response.md) werden aktualisiert, um Authentifizierungsinformationen in die HTTP Server Version 2.0-API aufzunehmen. [**HTTP \_ REQUEST \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) und [**HTTP REQUEST \_ \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) sind spezifisch für die Version der API, die von der Anwendung verwendet wird. Anwendungen sollten diese Strukturen jedoch nicht direkt in ihrem Code verwenden. Stattdessen sollten sie **HTTP \_ REQUEST** verwenden, um die richtige Version basierend auf der Version der Anforderungswarteschlange abzurufen, in der die Anforderung empfangen wurde. Beachten Sie außerdem, dass die Größe der **HTTP \_ REQUEST-Struktur** auf der Version des Betriebssystems basiert, unter dem der Code kompiliert wird.

 

 
