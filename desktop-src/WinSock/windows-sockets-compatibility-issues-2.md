---
description: Windows Sockets 2 unterstützt weiterhin alle Windows Sockets 1.1-Semantik und Funktionsaufrufe, mit Ausnahme derjenigen, die pseudoblockiert werden.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows Kompatibilitätsprobleme bei Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3fa7aba32ed74f04b04d717e0b2897dc92e0c78079d2a8c20e2c3bcdd85191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051468"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows Kompatibilitätsprobleme bei Sockets

Windows Sockets 2 unterstützt weiterhin alle Windows Sockets 1.1-Semantik und Funktionsaufrufe, mit Ausnahme derjenigen, die pseudoblockiert werden. Da Windows Sockets 2 nur in 32-Bit-Umgebungen mit präemptivem Zeitplan ausgeführt wird, ist es nicht erforderlich, die Pseudoblockierung in Windows Sockets 1.1 zu implementieren. Dies bedeutet, dass der WSAEINPROGRESS-Fehlercode nie angegeben wird und dass die folgenden Windows Sockets 1.1-Funktionen für Windows Sockets 2-Anwendungen nicht verfügbar sind:

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Windows Sockets 1.1-Programme, die zur Verwendung von Pseudoblockierung geschrieben wurden, funktionieren weiterhin ordnungsgemäß, da sie entweder mit Winsock.dll oder Wsock32.dll verknüpft sind. Beide unterstützen weiterhin den vollständigen Satz von Windows Sockets 1.1-Funktionen. Damit Programme Windows Sockets 2-Anwendungen werden, müssen einige Codeänderungen vorgenommen werden. In den meisten Fällen kann die wohlgemeinte Verwendung von Threads ersetzt werden, um die Verarbeitung zu ermöglichen, die mit einer blockierenden Hookfunktion durchgeführt wurde.

 

 



