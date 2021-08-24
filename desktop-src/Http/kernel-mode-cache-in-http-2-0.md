---
title: Kernelmoduscache
description: Kernelmoduscache
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34296ae6d0bca81988437478eb5893f1a7cb1b3c8a0dc2ae461356499bbfe10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340500"
---
# <a name="kernel-mode-cache"></a>Kernelmoduscache

Die HTTP Server Version 2.0-API ermöglicht Anwendungen das Zwischenspeichern von Antworten mit statischem Inhalt im Kernelmodus. Eine höhere Leistung wird erzielt, wenn Anforderungen aus dem Kernelcache bedient werden, ohne in den Benutzermodus zu wechseln.

Die HTTP-Server-API wendet die entsprechenden Eigenschaftenkonfigurationen auf alle Anforderungen an, die aus dem Kernelcache bereitgestellt werden, einschließlich Protokollierungsantworten. Anforderungen, die eine Authentifizierung erfordern, werden jedoch nicht aus dem Cache bedient.

Die HTTP-Server-API schränkt den Kernelmoduscache auf Anforderungen ein, die die folgenden Bedingungen erfüllen:

-   Das Anforderungsverb ist GET, und die gesamte Anforderung wird empfangen.
-   Die Anforderung darf keinen Entitätstext aufweisen.
-   Das HTTP-Protokoll ist Version 1.0 oder höher.
-   Der Header "Translate: f" ist nicht vorhanden.
-   Andere Header als "Expect: 100-Continue" sind nicht vorhanden.
-   Der Autorisierungsheader ist nicht vorhanden.
-   Die Header Range und If-Range sind nicht vorhanden.

Zusätzlich zu den Einschränkungen für die Anforderung muss die Antwort auch die folgenden Bedingungen erfüllen:

-   Die Antwortgröße ist standardmäßig auf 256 KB beschränkt. Um die Größe der zwischengespeicherten Antwort zu ändern, legen Sie den Registrierungswert **UriMaxUriBytes** auf die erforderliche Anzahl von Bytes fest.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   Die gesamte Antwort muss in einem einzigen Aufruf von [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)bereitgestellt werden.
-   Der Datumsheader in der Antwort darf nicht unterdrückt werden.
-   Wenn der Zuletzt geänderte Header vorhanden ist, muss der Wert des Headers die richtige Syntax aufweisen. Der Zeitwert in diesem Header wird für die Überprüfung des Cachesteuerelements verwendet.
-   Der Kernelmoduscache verfügt über genügend Speicherplatz, um die Antwort zu speichern.

Standardmäßig ist der Kernelmodus-Antwortcache aktiviert. Wenn eine der oben aufgeführten Bedingungen für die Anforderung oder Antwort nicht erfüllt ist, wird die Antwort gesendet, aber nicht zwischengespeichert. In der HTTP Server-API version 2.0 enthält [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) einen optionalen *pCachePolicy-Parameter,* um die [**HTTP CACHE \_ \_ POLICY-Struktur**](/windows/desktop/api/Http/ns-http-http_cache_policy) zu übergeben. Anwendungen verwenden die Cacherichtlinienstruktur, um den Cache zu konfigurieren.

 

 




