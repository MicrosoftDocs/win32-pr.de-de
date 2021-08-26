---
title: Threadsicherheit
description: Alle Funktionen in dieser API können sicher gleichzeitig aus verschiedenen Threads aufrufen. Jedes Objekt, das als Parameter an die Funktionen übergeben wird, hat jedoch ein bestimmtes Threadingverhalten, wie unten beschrieben.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Threadsicherheitswebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25528f3315fcfae95d07d973d4743548eb35ec84bf754fdaafe067bcaccc56f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054460"
---
# <a name="thread-safety"></a>Threadsicherheit

Alle Funktionen in dieser API können sicher gleichzeitig aus verschiedenen Threads aufrufen. Jedes Objekt, das als Parameter an die Funktionen übergeben wird, hat jedoch ein bestimmtes Threadingverhalten, wie unten beschrieben.


Die folgenden Handles sind Singlethread-Handles und unterstützen keine gleichzeitigen Vorgänge für eine bestimmte Instanz:

-   [\_WS-HEAP](ws-heap.md)
-   [\_WS-NACHRICHT](ws-message.md)
-   [WS \_ XML \_ BUFFER](ws-xml-buffer.md)
-   [\_ \_ WS-XML-READER](ws-xml-reader.md)
-   [WS \_ XML \_ WRITER](ws-xml-writer.md)
-   [\_WS-FEHLER](ws-error.md)
-   [\_WS-VORGANGSKONTEXT \_](ws-operation-context.md)
-   [\_WS-RICHTLINIE](ws-policy.md)
-   [\_WS-METADATEN](ws-metadata.md)
-   [\_ \_ WS-SICHERHEITSTOKEN](ws-security-token.md)
-   [\_WS-SICHERHEITSKONTEXT \_](ws-security-context.md)

Die folgenden Handles sind free-threaded und unterstützen gleichzeitige Vorgänge für eine bestimmte Instanz:

-   [\_WS-KANAL](ws-channel.md)
-   [\_WS-LISTENER](ws-listener.md)
-   [\_WS-DIENSTHOST \_](ws-service-host.md)
-   [\_WS-DIENSTPROXY \_](ws-service-proxy.md)

Für alle diese Handles wird Threading in Bezug auf Vorgänge (nicht Funktionsaufrufe) definiert. Ein Vorgang wird für synchron aufgerufene Funktionen anders definiert als für asynchron aufgerufene Funktionen:

-   Bei synchron aufgerufenen Funktionen steht der Vorgang während der Ausführung der Funktion aus.
-   Wenn die Funktion für asynchron aufgerufene Funktionen einen anderen Rückgabecode als **WS \_ S \_ ASYNC** zurückgibt, steht der Vorgang während der Ausführung der Funktion aus. Wenn die Funktion **jedoch WS \_ S \_ ASYNC** zurückgibt, steht der Vorgang aus, bis [**der WS \_ ASYNC \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) aufgerufen wird. Weitere Informationen zum asynchronen Aufrufen von Funktionen finden Sie im Thema [Asynchrones](asynchronous-model.md) Modell. Fehlercodes finden Sie unter [Windows Webdienste-Rückgabewerte.](windows-web-services-return-values.md)

Wenn der Threadingvertrag für ein Objekt nicht ausgeführt wird, führt dies zu nicht definiertem Verhalten.

 

 




