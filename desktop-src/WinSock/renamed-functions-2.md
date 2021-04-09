---
description: In zwei Fällen war es erforderlich, Funktionen umzubenennen, die in Berkeley Sockets verwendet werden, um Konflikte mit anderen Microsoft Windows-API-Funktionen zu vermeiden.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Umbenannte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863815"
---
# <a name="renamed-functions"></a>Umbenannte Funktionen

In zwei Fällen war es erforderlich, Funktionen umzubenennen, die in Berkeley Sockets verwendet werden, um Konflikte mit anderen Microsoft Windows-API-Funktionen zu vermeiden.

## <a name="close-and-closesocket"></a>Schließen und closesocket

Sockets werden von Standarddatei Deskriptoren in Berkeley Sockets dargestellt, sodass die **Close** -Funktion verwendet werden kann, um Sockets und normale Dateien zu schließen. Obwohl nichts in Windows Sockets verhindert, dass eine Implementierung reguläre Datei Handles verwendet, um Sockets zu identifizieren, ist dies nicht erforderlich. Unter Windows müssen Sockets mithilfe der [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Routine geschlossen werden. Unter Windows ist die Verwendung der **Close** -Funktion zum Schließen eines Sockets falsch, und die Auswirkungen, die dies bewirkt, sind durch diese Spezifikation nicht definiert.

## <a name="ioctl-and-ioctlsocketwsaioctl"></a>Ioctl und ioctlsocket/WSAIoctl

Verschiedene C-sprach Laufzeitsysteme verwenden IOCTLs für Zwecke, die nicht mit Windows Sockets verknüpft sind. Folglich wurden die [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) -Funktion und die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion definiert, um Socketfunktionen zu verarbeiten, die von **ioctl** und **fcntl** in der Berkeley-Software Verteilung durchgeführt wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> <dt>

[**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



