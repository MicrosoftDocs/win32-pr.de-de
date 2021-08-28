---
title: Funktionen der HTTP-Server-API, Version 2.0
description: Die HTTP-Server-API-Version 2.0 bietet die folgenden Funktionen.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funktionen der HTTP-Server-API, Version 2.0
- Functions HTTP, HTTP Server API Version 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b832a3f8fb1a97c48c49809d3e2f1975965becdc4c7bbf3942601d577d4702d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981360"
---
# <a name="http-server-api-version-20-functions"></a>Funktionen der HTTP-Server-API, Version 2.0

Die HTTP-Server-API-Version 2.0 bietet die folgenden Funktionen.

| Funktion | Beschreibung |
|-|-|
| [**HttpDelegateRequestEx**](/windows/win32/api/http/nf-http-httpdelegaterequestex) | Delegiert eine Anforderung aus der Quellanforderungswarteschlange an die Zielanforderungswarteschlange. |
| [**HttpFindUrlGroupId**](/windows/win32/api/http/nf-http-httpfindurlgroupid) | Ruft eine URL-Gruppen-ID für eine URL und eine Anforderungswarteschlange ab. |
| [**HttpIsFeatureSupported**](/windows/win32/api/http/nf-http-httpisfeaturesupported) | Überprüft, ob ein bestimmtes Feature unterstützt wird. |

## <a name="server-session"></a>Serversitzung

| Funktion | Beschreibung |
|-|-|
| [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a>URL-Gruppen

| Funktion | Beschreibung |
|-|-|
| [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a>Anforderungs-Warteschlange

| Funktion | Beschreibung |
|-|-|
| [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [**HttpShutdownRequestQueue**](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a>Zugehörige Themen

[HTTP-Server-API-Strukturen der Version 2.0](http-server-api-version-2-0-structures.md)
