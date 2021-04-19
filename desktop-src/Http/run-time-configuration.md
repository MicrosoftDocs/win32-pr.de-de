---
title: Run-Time Konfiguration
description: Die HTTP-API ermöglicht es Anwendungen, zur Laufzeit dynamische Konfigurationen auszuführen.
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b0a310f9fe86b2e6972aa2dff3d3b7fc05965
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342283"
---
# <a name="run-time-configuration"></a>Run-Time Konfiguration

Die HTTP-API ermöglicht es Anwendungen, zur Laufzeit dynamische Konfigurationen auszuführen. Die Laufzeitkonfiguration ist nicht persistent, erfordert nur Berechtigungen auf niedriger Ebene und wirkt sich nur auf Ihre Anwendung aus. Zur Laufzeitkonfiguration können folgende Aktivitäten gehören:

-   Initialisieren des HTTP-Dienst und Erstellen einer Server Sitzung. Eine Anwendung initialisiert den HTTP-Dienst durch Aufrufen der [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) -Funktion. Der Server muss initialisiert werden, bevor andere Serverfunktionen aufgerufen werden können. Die Anwendung erstellt dann eine Server Sitzung durch Aufrufen der Funktion [**httpcreateserversession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) . Die Server Sitzung ist ein Container für Eigenschaften, die über alle URL-Gruppen hinweg gelten, die zu dieser Server Sitzung gehören. In der Regel verfügt jede Verbindung nur über eine Server Sitzung. Informationen zum Festlegen von Server Sitzungs Eigenschaften und deren Gültigkeitsbereich finden Sie unter [**httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).
-   Registrieren für URLs Nachdem die Server Sitzung erstellt wurde, kann eine Anwendung für URLs registriert werden, indem eine oder mehrere URL-Gruppen erstellt werden. Eine URL-Gruppe ist eine Gruppe von URLs, auf die die gleichen Eigenschaften angewendet werden. Eine Anwendung erstellt eine URL-Gruppe durch Aufrufen der [**httpcreateurlgroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) -Funktion und fügt dann die gewünschten URLs hinzu, indem Sie die [**httpaddurltourlgroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) -Funktion aufrufen. Nachdem eine Anwendung für URLs registriert wurde, indem Sie eine URL-Gruppe erstellt und die URL-Gruppe mit einer Anforderungs Warteschlange verknüpft hat (siehe [Erstellen und Binden an eine Anforderungs Warteschlange](creating-and-binding-to-a-request-queue.md)), werden alle aus diesen URLs kommenden Anforderungen an die Anforderungs Warteschlange weitergeleitet, die dieser Anwendung zugeordnet ist. Weitere Informationen zum Festlegen von Eigenschaften von URL-Gruppen finden Sie unter [ **httpseturlgroupproperty** .](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   Aktivieren von Funktionen durch Festlegen von http-Server Eigenschaften, z. b. [Authentifizierung](authentication-in-http-version-2-0.md), [Protokollierung](server-side-logging-in-http-version-2-0.md), QoS-Einstellungen, Timeouts, aktivierter Status und Bindungs Informationen. Weitere Informationen zum Festlegen von Eigenschaften finden Sie unter [**http- \_ Server \_ Eigenschaft**](/windows/desktop/api/Http/ne-http-http_server_property).

 

 




