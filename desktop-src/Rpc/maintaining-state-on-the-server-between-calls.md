---
title: Beibehalten des Zustands auf dem Server zwischen Aufrufen
description: Es ist häufig erforderlich, den Zustand auf dem Server zwischen separaten RPC-Aufrufen \ 8212 zu verwalten. Die Verwendung von Kontexthandles ist die beste Möglichkeit. Ein paar Wörter zur internen Funktionsweise von Kontexthandles helfen dabei zu verstehen, wann Kontexthandles am besten funktionieren.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC für Remoteprozeduraufrufe, bewährte Methoden, Beibehalten des Zustands zwischen Aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e564acbb4748cd76988c1b064a58ede2169d3d20da4033774f3141883a7193bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928585"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Beibehalten des Zustands auf dem Server zwischen Aufrufen

Es ist häufig erforderlich, den Zustand auf dem Server zwischen separaten RPC-Aufrufen zu verwalten. Die Verwendung von Kontexthandles ist die beste Möglichkeit. Ein paar Wörter zur internen Funktionsweise von Kontexthandles helfen dabei zu verstehen, wann Kontexthandles am besten funktionieren.

Der Client empfängt nie den Zustand, der auf dem Server beibehalten wird. Meistens ist der Zustand auf dem Server ein Zeiger auf einen Speicherblock, und der Client verfügt über keine Informationen dazu. Der Client erhält nur eine große eindeutige Zahl mit anderen informationen, die der Server an den Client sendet und die das Kontexthand handle in allen nachfolgenden Vorgängen darstellt. Wenn der Client auf ein geöffnetes Handle verweist, sendet er die große Zahl, die er vom Server empfangen hat, als dieses Kontexthand handle geöffnet wurde.

Der Server verfolgt alle großen Zahlen nach, die er an einen Client sendet. Wenn der Server eine große Zahl empfängt, die ein Kontexthandles darstellt, sucht er die Zahl in der Auflistung gültiger, ausstehender Kontexthandles für diesen Client und sucht den serverseitigen Kontext, der einer bestimmten großen Zahl entspricht. Dies wird an die Serverroutine übergeben. Wenn die große Zahl nicht gefunden wird, wird eine RPC X SS CONTEXT MISMATCH-Ausnahme ausgelöst und an \_ \_ den Client \_ \_ propagiert.

Die Corollaries dieses Entwurfs lauten wie folgt:

-   Ein Kontexthand handle ist nur im Kontext der vorhandenen Client-/Serversitzung gültig. Sie kann nicht an einen anderen Client übergeben werden.
-   Ein Kontexthandl wird ungültig, wenn der Server neu gestartet wird oder die Verbindung mit dem Client auf andere Weise verloren geht.
-   Der Client kann nicht interpretieren, was das Kontexthandy auf dem Server darstellt. Für einen Client sind alle Kontexthandles einfach große Zahlen.

Wenn der Client ausfällt, wird dem Server eine Benachrichtigung angezeigt, und seine Kontexthandles werden mithilfe des Run-Down-Mechanismus bereinigt.

 

 




