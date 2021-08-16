---
title: Run-Time Konfiguration
description: Mit der HTTP-API können Anwendungen zur Laufzeit eine dynamische Konfiguration durchführen.
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b240438ada7fce186f334df3175b8ecc5b557626c5f1f085cdf82965fb32365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393752"
---
# <a name="run-time-configuration"></a>Run-Time Konfiguration

Mit der HTTP-API können Anwendungen zur Laufzeit eine dynamische Konfiguration durchführen. Die Laufzeitkonfiguration ist nicht persistent, erfordert nur geringe Berechtigungen und wirkt sich nur auf Ihre Anwendung aus. Die Laufzeitkonfiguration kann eine der folgenden Aktivitäten umfassen:

-   Initialisieren des HTTP-Diensts und Erstellen einer Serversitzung. Eine Anwendung initialisiert den HTTP-Dienst durch Aufrufen der [**HttpInitialize-Funktion.**](/windows/desktop/api/Http/nf-http-httpinitialize) Der Server muss initialisiert werden, bevor andere Serverfunktionen aufgerufen werden können. Die Anwendung erstellt dann eine Serversitzung, indem sie die [**HttpCreateServerSession-Funktion**](/windows/desktop/api/Http/nf-http-httpcreateserversession) aufruft. Die Serversitzung ist ein Container für Eigenschaften, die für alle URL-Gruppen gelten, die zu dieser Serversitzung gehören. In der Regel verfügt jede Allication nur über eine Serversitzung. Informationen zum Festlegen von Serversitzungseigenschaften und zu deren Bereich finden Sie unter [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).
-   Registrieren für URLs. Nachdem die Serversitzung erstellt wurde, kann sich eine Anwendung für URLs registrieren, indem eine oder mehrere URL-Gruppen erstellt werden. Eine URL-Gruppe ist eine Gruppe von URLs, auf die die gleichen Eigenschaften angewendet werden. Eine Anwendung erstellt eine URL-Gruppe durch Aufrufen der [**HttpCreateUrlGroup-Funktion**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) und fügt dann die gewünschten URLs hinzu, indem sie die [**HttpAddUrlToUrlGroup-Funktion**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) aufruft. Nachdem sich eine Anwendung durch Erstellen einer URL-Gruppe für URLs registriert [](creating-and-binding-to-a-request-queue.md)und die URL-Gruppe einer Anforderungswarteschlange zugeordnet hat (siehe Erstellen und Binden an eine Anforderungswarteschlange), werden alle Von diesen URLs gesendeten Anforderungen an die Anforderungswarteschlange geroutet, die dieser Anwendung zugeordnet ist. Weitere Informationen zum Festlegen von URL-Gruppeneigenschaften finden Sie unter [ **HttpSetUrlGroupProperty.**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   Aktivieren von Features durch Festlegen von [](authentication-in-http-version-2-0.md)HTTP-Servereigenschaften, z. B. Authentifizierung, [Protokollierung,](server-side-logging-in-http-version-2-0.md)QOS-Einstellungen, Timeouts, aktivierter Status und Bindungsinformationen. Informationen zum Festlegen von Eigenschaften finden Sie unter [**HTTP \_ SERVER \_ PROPERTY**](/windows/desktop/api/Http/ne-http-http_server_property).

 

 




