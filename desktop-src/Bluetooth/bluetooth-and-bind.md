---
title: Bluetooth und Binden
description: Bluetooth verwendet die Bind-Funktion zum Binden an einen Socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth und Binden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7e7571e8d8a2c1a6dee29dc5f4839af5f1064bc5351cd3a13937f5750dd04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588490"
---
# <a name="bluetooth-and-bind"></a>Bluetooth und Binden

Bluetooth verwendet die [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) zum Binden an einen Socket. Um einen Bluetooth Socket zu binden, rufen Sie die **Bind-Funktion** mithilfe der [**SOCKADDR \_ BTH-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) auf. Verwenden Sie die **SOCKADDR \_ BTH-Struktur** mit den folgenden Einstellungen:

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

In Clientanwendungen muss das Portmitglied 0 (null) sein, damit ein geeigneter lokaler Endpunkt zugewiesen werden kann. In Serveranwendungen muss der Portmember eine gültige Portnummer oder BT \_ PORT \_ ANY sein. Ports, die automatisch über BT PORT ANY zugewiesen werden, \_ können anschließend mit einem Aufruf der \_ [**getsockname-Funktion**](bluetooth-and-getsockname.md) abgefragt werden. Der gültige Bereich für die Anforderung eines bestimmten RFCOMM-Ports beträgt 1 bis 30. Serverkanäle sind globale Ressourcen, und nur 30 Serverkanäle sind für RFCOMM auf allen Bluetooth Geräten verfügbar, die von allen Windows Sockets gemeinsam genutzt werden müssen, die zur Bluetooth-Adressfamilie gehören. Wenn kein Serverkanal verfügbar ist oder der angegebene Serverkanal bereits reserviert ist, schlägt der [**Bindungsaufruf**](/windows/desktop/api/winsock/nf-winsock-bind) fehl.

Nach erfolgreicher Rückgabe aus der Bindung wird der Serverkanal reserviert, bis der Socket geschlossen wird. Verwenden Sie die [**Getsockname-Funktion,**](bluetooth-and-getsockname.md) um die Kanalnummer für die SDP-Registrierung abzurufen.

Anwendungen sollten die automatische Zuordnung für den Serverkanal verwenden.

Die [**Bind-Funktion**](/windows/desktop/api/winsock/nf-winsock-bind) kündigt die Serveranwendung nicht automatisch mithilfe des Bluetooth-SDP an. -Anwendungen müssen die [**WSASetService-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) aufrufen, um von Remoteanwendungen Bluetooth gefunden zu werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Binden**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 