---
title: Threadsicherheit
description: Alle Funktionen in dieser API können gleichzeitig von verschiedenen Threads aus aufgerufen werden. Jedes Objekt, das als Parameter an die Funktionen übergeben wird, hat jedoch ein bestimmtes Threading Verhalten, wie unten beschrieben.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Thread Sicherheit-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734849"
---
# <a name="thread-safety"></a>Threadsicherheit

Alle Funktionen in dieser API können gleichzeitig von verschiedenen Threads aus aufgerufen werden. Jedes Objekt, das als Parameter an die Funktionen übergeben wird, hat jedoch ein bestimmtes Threading Verhalten, wie unten beschrieben.


Die folgenden Handles sind Single Thread und unterstützen keine gleichzeitigen Vorgänge für eine bestimmte Instanz:

-   [WS- \_ Heap](ws-heap.md)
-   [WS- \_ Nachricht](ws-message.md)
-   [WS- \_ XML- \_ Puffer](ws-xml-buffer.md)
-   [WS- \_ XML- \_ Reader](ws-xml-reader.md)
-   [WS- \_ XML- \_ Writer](ws-xml-writer.md)
-   [WS- \_ Fehler](ws-error.md)
-   [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md)
-   [WS- \_ Richtlinie](ws-policy.md)
-   [WS- \_ Metadaten](ws-metadata.md)
-   [WS- \_ Sicherheits \_ Token](ws-security-token.md)
-   [WS- \_ Sicherheits \_ Kontext](ws-security-context.md)

Die folgenden Handles sind frei Thread und unterstützen gleichzeitige Vorgänge für eine bestimmte Instanz:

-   [WS- \_ Kanal](ws-channel.md)
-   [WS- \_ Listener](ws-listener.md)
-   [WS- \_ Dienst \_ Host](ws-service-host.md)
-   [WS- \_ Dienst \_ Proxy](ws-service-proxy.md)

Für all diese Handles wird Threading in Bezug auf Vorgänge (nicht Funktionsaufrufe) definiert. Ein Vorgang wird für Funktionen, die synchron aufgerufen werden, anders definiert als bei Funktionen, die asynchron aufgerufen werden:

-   Bei Funktionen, die synchron aufgerufen werden, steht der Vorgang während der Ausführung der Funktion aus.
-   Für Funktionen, die asynchron aufgerufen werden, ist der Vorgang während der Ausführung der Funktion ausstehend, wenn die Funktion einen anderen Rückgabecode als **WS \_ S \_** zurückgibt. Wenn die Funktion jedoch **WS \_ S \_ Async** zurückgibt, ist der Vorgang bis zum Aufruf des asynchronen [**WS- \_ \_ Rückrufs**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) ausstehend. Weitere Informationen zum asynchronen Aufrufen von Funktionen finden Sie im Thema zum [asynchronen Modell](asynchronous-model.md) . Fehlercodes finden Sie unter [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md).

Wenn der Threading Vertrag für ein Objekt nicht befolgt wird, führt dies zu einem nicht definierten Verhalten.

 

 




