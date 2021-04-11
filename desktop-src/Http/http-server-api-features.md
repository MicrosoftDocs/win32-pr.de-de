---
title: HTTP-Server-API-Funktionen
description: In diesem Thema werden und nicht unterstützte Funktionen der HTTP-Server-API unterstützt.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- HTTP-Server-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310999"
---
# <a name="http-server-api-features"></a>HTTP-Server-API-Funktionen

In der folgenden Liste werden die unterstützten und nicht unterstützten Funktionen der HTTP-Server-API beschrieben.

## <a name="features-supported"></a>Unterstützte Features

HTTP unterstützt die folgenden Funktionen:

-   HTTP v 1.0-und v 1.1-Serverfunktionen.
-   Secure Sockets Layer 3,0 (SSL) mit Unterstützung für Client-und Server Zertifikate.
-   Zwischenspeichern von Daten Fragmenten zur Verwendung in nachfolgenden Antworten.
-   Unterstützung für IPv6-und IPv4-Adressierung.
-   URL-Namespace Reservierungen für die Anwendungssicherheit.
-   True-Handles für alle-Objekte.
-   Synchrone und asynchrone e/a-Modelle.
-   Unterstützung für WOW64 auf Computern unter 64-Bit-Windows ab Windows Server 2003 mit Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Nicht unterstützte Funktionen

Die HTTP-Server-API unterstützt nicht die folgenden Funktionen:

-   Die HTTP-Server-API führt keine Client-oder Server Authentifizierung basierend auf dem Inhalt der HTTP-Anforderungs Header aus. Die erforderliche Authentifizierung muss von der Anwendung implementiert werden.
-   WOW64 auf Computern, die auf 64-Bit-Windows-Computern ausgeführt werden, wird unter Windows Server 2003 und Windows XP mit Service Pack 2 (SP2) und früher nicht unterstützt.
-   Die HTTP-Server-API unterstützt keine Protokollierung von HTTP-Anforderungen und-Antworten.
-   Die HTTP-Server-API segmentieren ausgehende HTTP-Antworten nicht. Die Anwendung muss bei Bedarf die Antwort Segmentierung implementieren.

 

 




