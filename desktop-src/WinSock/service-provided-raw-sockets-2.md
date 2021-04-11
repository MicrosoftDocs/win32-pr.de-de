---
description: Ein unformatierte Socket ist ein Typ von Socket, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht. Die Verwendung von rohsockets beim Portieren von Anwendungen auf Winsock wird aus verschiedenen Gründen nicht empfohlen.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Rohdaten Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131024"
---
# <a name="raw-sockets"></a>Rohdaten Sockets

Ein unformatierte Socket ist ein Typ von Socket, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht. Die Verwendung von rohsockets beim Portieren von Anwendungen auf Winsock wird aus verschiedenen Gründen nicht empfohlen.

Die Windows Sockets-Spezifikation gibt nicht an, dass ein Winsock-Dienstanbieter Rohdaten Sockets unterstützt, d. h. Sockets vom Typ " **Sock \_ RAW**". Dienstanbieter werden jedoch empfohlen, RAW Socket-Unterstützung bereitzustellen. Eine Windows Sockets-kompatible Anwendung, die unformatierte Sockets verwenden möchte, sollte versuchen, den Socket mit dem [**socketbefehl**](/windows/desktop/api/Winsock2/nf-winsock2-socket) zu öffnen, und wenn Sie fehlschlägt, versuchen Sie, einen anderen Sockettyp zu verwenden, oder geben Sie den Fehler des Benutzers an.

Unter Windows 7, Windows Server 2008 R2, Windows Vista und Windows XP mit Service Pack 2 (SP2) wurde die Möglichkeit zum Senden von Datenverkehr über Unformatierte Sockets auf verschiedene Weise eingeschränkt. Weitere Informationen finden Sie unter [TCP/IP-rohsockets](tcp-ip-raw-sockets-2.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Glühbirne**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[TCP/IP-Rohdaten Sockets](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 



