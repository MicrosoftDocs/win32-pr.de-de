---
title: HTTP-Server-API-Funktionen
description: Dieses Thema unterstützte und nicht unterstützte Funktionen der HTTP-Server-API.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- HTTP-Server-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaf567d4576618b07ef5ad8dec91b360f37ab46eb820ff52e2bca896ca91a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014778"
---
# <a name="http-server-api-features"></a>HTTP-Server-API-Funktionen

In den folgenden Listen werden die unterstützten und nicht unterstützten Funktionen der HTTP-Server-API beschrieben.

## <a name="features-supported"></a>Unterstützte Features

HTTP unterstützt die folgenden Features:

-   Http v1.0- und v1.1-Serverfunktionen.
-   Secure Sockets Layer 3.0 (SSL) mit Unterstützung für Client- und Serverzertifikate.
-   Zwischenspeichern von Datenfragmenten zur Verwendung in nachfolgenden Antworten.
-   Unterstützung für IPv6- und IPv4-Adressierung.
-   URL-Namespacereservierungen für die Anwendungssicherheit.
-   True-Handles für alle -Objekte.
-   Synchrone und asynchrone E/A-Modelle.
-   Unterstützung für WOW64 auf Computern mit 64-Bit-Windows ab Windows Server 2003 mit Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Nicht unterstützte Features

Die HTTP-Server-API unterstützt die folgenden Funktionen nicht:

-   Die HTTP-Server-API führt keine Client- oder Serverauthentifizierung basierend auf dem Inhalt der HTTP-Anforderungsheader durch. Alle erforderlichen Authentifizierungen müssen von der Anwendung implementiert werden.
-   WOW64 auf Computern, die auf 64-Bit-Windows ausgeführt werden, wird unter Windows Server 2003 und Windows XP mit Service Pack 2 (SP2) und früher nicht unterstützt.
-   Die HTTP-Server-API unterstützt keine Protokollierung von HTTP-Anforderungen und -Antworten.
-   Die HTTP-Server-API blockt keine ausgehenden HTTP-Antworten. Die Anwendung muss bei Bedarf eine Antwort chunking implementieren.

 

 




