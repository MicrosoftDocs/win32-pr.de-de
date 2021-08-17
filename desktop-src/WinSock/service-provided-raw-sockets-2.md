---
description: Ein unformatiertes Socket ist ein Sockettyp, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht. Die Verwendung von unformatierten Sockets beim Portieren von Anwendungen zu Winsock wird aus verschiedenen Gründen nicht empfohlen.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Rohdatensockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c1522c2b8499e2ba8f1bb693513105804ec936fc2224fccaa55dd90a1b0dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740534"
---
# <a name="raw-sockets"></a>Rohdatensockets

Ein unformatiertes Socket ist ein Sockettyp, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht. Die Verwendung von unformatierten Sockets beim Portieren von Anwendungen zu Winsock wird aus verschiedenen Gründen nicht empfohlen.

Die Windows Sockets-Spezifikation schreibt nicht vor, dass ein Winsock-Dienstanbieter Unformatierte Sockets unterstützt, d. h. Sockets vom Typ **SOCK \_ RAW**. Dienstanbietern wird jedoch empfohlen, Unterstützung für unformatierte Sockets zu bieten. Eine Windows Sockets-kompatible Anwendung, die Unformatierte Sockets verwenden möchte, sollte versuchen, den Socket mit dem [**Socketaufruf**](/windows/desktop/api/Winsock2/nf-winsock2-socket) zu öffnen. Wenn der Socketaufruf fehlschlägt, sollte entweder versucht werden, einen anderen Sockettyp zu verwenden, oder der Benutzer sollte den Fehler angeben.

Auf Windows 7, Windows Server 2008 R2, Windows Vista und Windows XP mit Service Pack 2 (SP2) wurde die Möglichkeit zum Senden von Datenverkehr über Unformatierte Sockets auf verschiedene Weise eingeschränkt. Weitere Informationen finden Sie unter [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Portieren von Socketanwendungen in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[UNFORMATIERTE TCP/IP-Sockets](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 



