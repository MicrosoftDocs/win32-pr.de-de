---
title: Kernelmoduscache
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037502"
---
# <a name="kernel-mode-cache"></a>Kernelmoduscache

Die HTTP-Server Version 2,0-API ermöglicht Anwendungen das Zwischenspeichern von Antworten mit statischen Inhalten im Kernel Modus. Eine bessere Leistung wird erzielt, wenn Anforderungen aus dem Kernel Cache bereitgestellt werden, ohne in den Benutzermodus übergeht.

Die HTTP-Server-API wendet die entsprechenden Eigenschaften Konfigurationen auf alle Anforderungen aus dem Kernel Cache an, einschließlich Protokollierungs Antworten. Anforderungen, die eine Authentifizierung erfordern, werden jedoch nicht aus dem Cache bedient.

Die HTTP-Server-API schränkt den Kernelmoduscache auf Anforderungen ein, die die folgenden Bedingungen erfüllen:

-   Das Anforderungs Verb lautet Get, und die gesamte Anforderung wird empfangen.
-   Die Anforderung darf keinen Entitäts Text enthalten.
-   Das HTTP-Protokoll ist Version 1,0 oder höher.
-   Der Header "Translation: f" ist nicht vorhanden.
-   Erwarten Sie, dass keine anderen Header als "erwartet: 100-Continue" vorhanden sind.
-   Der Autorisierungs Header ist nicht vorhanden.
-   Die Header Range und If-Range sind nicht vorhanden.

Zusätzlich zu den Einschränkungen für die Anforderung muss die Antwort auch die folgenden Bedingungen erfüllen:

-   Die Antwort Größe ist standardmäßig auf 256 KB beschränkt. Um die Größe der zwischengespeicherten Antwort zu ändern, legen Sie für den Registrierungs Wert **urimaxuribytes** die erforderliche Anzahl von Bytes fest.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   Die gesamte Antwort muss in einem einzelnen [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)-Befehl angegeben werden.
-   Der Date-Header für die Antwort darf nicht unterdrückt werden.
-   Wenn der Last-modified-Header vorhanden ist, muss der Wert des-Headers über die korrekte Syntax verfügen. Der Uhrzeitwert in diesem Header wird zur Überprüfung der Cache Steuerung verwendet.
-   Der Kernelmoduscache verfügt über genügend Speicherplatz zum Speichern der Antwort.

Standardmäßig ist der Kernel Modus-Antwort Cache aktiviert. Wenn eine der Bedingungen für die oben aufgeführte Anforderung oder Antwort nicht erfüllt ist, wird die Antwort gesendet, Sie wird jedoch nicht zwischengespeichert. In der HTTP-Server Version 2,0-API enthält [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) einen optionalen *pcachepolicy* -Parameter, um die [**http- \_ Cache \_ Richtlinien**](/windows/desktop/api/Http/ns-http-http_cache_policy) Struktur zu übergeben. Anwendungen verwenden die Cache Richtlinien Struktur, um den Cache zu konfigurieren.

 

 




