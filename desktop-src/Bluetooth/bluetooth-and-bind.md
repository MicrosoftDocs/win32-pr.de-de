---
title: Bluetooth und BIND
description: Bluetooth verwendet die Bind-Funktion, um eine Bindung an einen Socket herzustellen.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth und BIND
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858448"
---
# <a name="bluetooth-and-bind"></a>Bluetooth und BIND

Bluetooth verwendet die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion, um eine Bindung an einen Socket herzustellen. Um einen Bluetooth-Socket zu binden, können Sie die **Bind** -Funktion mithilfe der [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur abrufen. Verwenden Sie die **sockaddr- \_ BTH** -Struktur mit den folgenden Einstellungen:

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

Bei Client Anwendungen muss der portmember NULL sein, damit ein geeigneter lokaler Endpunkt zugewiesen werden kann. Bei Server Anwendungen muss es sich bei dem Porttyp um eine gültige Portnummer oder einen BT-Port handeln, und \_ \_ Ports, die mithilfe des BT-Ports automatisch zugewiesen \_ werden, \_ können anschließend mit einem Aufrufen der [**getsockname**](bluetooth-and-getsockname.md) -Funktion abgefragt werden. Der gültige Bereich für die Anforderung eines bestimmten RFCOMM-Ports liegt zwischen 1 und 30. Server Kanäle sind globale Ressourcen, und für RFCOMM sind nur 30 Server Kanäle auf allen Bluetooth-Geräten verfügbar, die von allen Windows-Sockets gemeinsam genutzt werden müssen, die zur Bluetooth-Adressfamilie gehören. Wenn kein Serverchannel verfügbar ist oder der angegebene Serverchannel bereits reserviert ist, schlägt der [**Bindungs**](/windows/desktop/api/winsock/nf-winsock-bind) Befehl fehl.

Nach erfolgreicher Rückgabe von BIND wird der Serverchannel reserviert, bis der Socket geschlossen wird. Verwenden Sie die Funktion [**getsockname**](bluetooth-and-getsockname.md) , um die Kanalnummer für die SDP-Registrierung abzurufen.

Anwendungen sollten die automatische Zuordnung für den Serverchannel verwenden.

Die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion kündigt die Serveranwendung nicht automatisch mit dem Bluetooth-SDP an. Anwendungen müssen die [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) -Funktion abrufen, die von Bluetooth-Remote Anwendungen gefunden werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Zwick**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 