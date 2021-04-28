---
title: Kernelmoduscache
description: Kernelmoduscache
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c409b00da03c0550899f5d26c4e6a0fa215118
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090888"
---
# <a name="kernel-mode-cache"></a>Kernelmoduscache

Mit der HTTP Server-API Version 2.0 können Anwendungen Antworten mit statischem Inhalt im Kernelmodus zwischenspeichern. Eine höhere Leistung wird erzielt, wenn Anforderungen aus dem Kernelcache bedient werden, ohne in den Benutzermodus zu wechseln.

Die HTTP-Server-API wendet die entsprechenden Eigenschaftenkonfigurationen auf alle Anforderungen an, die vom Kernelcache bereitgestellt werden, einschließlich der Protokollierung von Antworten. Anforderungen, die eine Authentifizierung erfordern, werden jedoch nicht aus dem Cache bereitgestellt.

Die HTTP-Server-API beschränkt den Cache im Kernelmodus auf Anforderungen, die die folgenden Bedingungen erfüllen:

-   Das Anforderungsverb ist GET, und die gesamte Anforderung wird empfangen.
-   Die Anforderung darf keinen Entitätskörper haben.
-   Das HTTP-Protokoll ist Version 1.0 oder höher.
-   Der Header "Translate: f" ist nicht vorhanden.
-   Es sind keine anderen Header als "Expect: 100-Continue" vorhanden.
-   Der Autorisierungsheader ist nicht vorhanden.
-   Die Range- If-Range-Header sind nicht vorhanden.

Zusätzlich zu den Einschränkungen für die Anforderung muss die Antwort auch die folgenden Bedingungen erfüllen:

-   Die Antwortgröße ist standardmäßig auf 256 KB beschränkt. Um die Größe der zwischengespeicherten Antwort zu ändern, legen Sie den **Registrierungswert UriMaxUriBytes** auf die erforderliche Anzahl von Bytes fest.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   Die gesamte Antwort muss in einem einzigen Aufruf von [**HttpSendHttpResponse bereitgestellt werden.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)
-   Der Datumsheader in der Antwort darf nicht unterdrückt werden.
-   Wenn der Zuletzt geänderte Header vorhanden ist, muss der Wert des Headers die richtige Syntax aufweisen. Der Zeitwert in diesem Header wird für die Überprüfung des Cachesteuerelements verwendet.
-   Der Kernelmoduscache verfügt über genügend Speicherplatz, um die Antwort zu speichern.

Standardmäßig ist der Kernelmodus-Antwortcache aktiviert. Wenn eine der oben aufgeführten Bedingungen für die Anforderung oder Antwort nicht erfüllt ist, wird die Antwort gesendet, aber nicht zwischengespeichert. In der HTTP Server-API version 2.0 enthält [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) einen optionalen *pCachePolicy-Parameter,* um die [**HTTP CACHE \_ \_ POLICY-Struktur**](/windows/desktop/api/Http/ns-http-http_cache_policy) zu übergeben. Anwendungen verwenden die Cacherichtlinienstruktur, um den Cache zu konfigurieren.

 

 




