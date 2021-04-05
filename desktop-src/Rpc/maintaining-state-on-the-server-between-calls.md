---
title: Beibehalten des Zustands auf dem Server zwischen Aufrufen
description: Es ist häufig erforderlich, den Zustand auf dem Server zwischen separaten RPC-Aufrufen \ 8212 beizubehalten. die Verwendung von Kontext Handles ist die beste Möglichkeit. Mit wenigen Worten, wie Kontext Handles intern funktionieren, hilft Ihnen zu verstehen, wann Kontext Handles am besten funktionieren.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, aufrechterhalten des Zustands zwischen Aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707187"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Beibehalten des Zustands auf dem Server zwischen Aufrufen

Es ist häufig erforderlich, den Zustand auf dem Server zwischen separaten RPC-Aufrufen beizubehalten – mithilfe von Kontext Handles ist dies die beste Möglichkeit. Mit wenigen Worten, wie Kontext Handles intern funktionieren, hilft Ihnen zu verstehen, wann Kontext Handles am besten funktionieren.

Der Client erhält nie den Status, der auf dem Server beibehalten wird. In den meisten Fällen ist der Status auf dem Server ein Zeiger auf einen Speicherblock, und der Client hat keine Informationen dazu. Alle Client Empfangs Vorgänge sind eine große eindeutige Zahl, mit anderen Informationen, die vom Server an den Client gesendet werden und die das Kontext Handle in allen nachfolgenden Vorgängen darstellt. Wenn sich der Client auf ein geöffnetes Handle bezieht, sendet es die große Zahl, die er vom Server empfangen hat, als dieses Kontext Handle geöffnet wurde.

Der Server verfolgt alle großen Zahlen, die er an einen Client sendet. Wenn der Server eine große Zahl empfängt, die ein Kontext Handle darstellt, sucht er die Zahl in der Auflistung gültiger, ausstehender Kontext Handles für diesen Client und sucht den serverseitigen Kontext, der einer bestimmten großen Zahl entspricht. Diese wird an die Server Routine übergeben. Wenn die große Zahl nicht gefunden wird, wird eine RPC \_ X \_ SS \_ -Kontext Konflikt \_ Ausnahme ausgelöst und an den Client weitergegeben.

Dies sind die folgenden:

-   Ein Kontext Handle ist nur im Kontext der vorhandenen Client-/Serversitzung gültig. Sie kann nicht an einen anderen Client übermittelt werden.
-   Ein Kontext Handle wird ungültig, wenn der Server neu gestartet wird oder andernfalls seine Verbindung mit dem Client verliert.
-   Der Client kann nicht interpretieren, was das Kontext Handle auf dem Server darstellt. Für einen Client sind alle Kontext Handles einfach eine große Zahl.

Wenn der Client fehlschlägt, erhält der Server eine Benachrichtigung, und die Kontext Handles werden mithilfe des-Lauf Mechanismus bereinigt.

 

 




