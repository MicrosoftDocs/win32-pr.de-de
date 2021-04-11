---
description: Windows Sockets 2 unterstützt weiterhin alle Semantik-und Funktionsaufrufe von Windows Sockets 1,1, mit Ausnahme derjenigen, die mit der Pseudo Blockierung arbeiten.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows Sockets-Kompatibilitätsprobleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214989"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows Sockets-Kompatibilitätsprobleme

Windows Sockets 2 unterstützt weiterhin alle Semantik-und Funktionsaufrufe von Windows Sockets 1,1, mit Ausnahme derjenigen, die mit der Pseudo Blockierung arbeiten. Da Windows Sockets 2 nur in den in 32-Bit-Umgebungen, in der voremptiv geplanten Umgebungen, ausgeführt wird, ist es nicht erforderlich, die in Windows Sockets 1,1 gefundene Pseudo Blockierung zu implementieren. Dies bedeutet, dass der wsaan Progress-Fehlercode nie angezeigt wird und dass die folgenden Windows Sockets 1,1-Funktionen für Windows Sockets 2-Anwendungen nicht verfügbar sind:

-   Wsacancelblockingcall
-   Wsais-Blockierung
-   Wsasetblockinghook
-   Wsaunhuokblockinghook

Windows Sockets 1,1-Programme, die zur Verwendung von Pseudo Blockierungen geschrieben werden, funktionieren weiterhin ordnungsgemäß, da Sie mit Winsock.dll oder Wsock32.dll verknüpft sind. Beide unterstützen weiterhin den kompletten Satz von Windows Sockets 1,1-Funktionen. Damit Programme zu Windows Sockets 2-Anwendungen werden können, muss eine Änderung des Codes erfolgen. In den meisten Fällen kann die kluge Verwendung von Threads durch die Verarbeitung der Verarbeitung ersetzt werden, die mit einer blockierenden Hook-Funktion erreicht wurde.

 

 



