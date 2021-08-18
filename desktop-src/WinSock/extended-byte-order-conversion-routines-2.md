---
description: Windows Sockets 2 geht nicht davon aus, dass die Netzwerk-Bytereihenfolge für alle Protokolle identisch ist.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Erweiterte Byte-Order-Konvertierungsroutinen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2be1c217e89d19e607a64dfc943449351021506dc88f73ebcd4234a26b2b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132523"
---
# <a name="extended-byte-order-conversion-routines"></a>Erweiterte Byte-Order-Konvertierungsroutinen

Windows Sockets 2 geht nicht davon aus, dass die Netzwerk-Bytereihenfolge für alle Protokolle identisch ist. Für die Konvertierung von 16-Bit- und 32-Bit-Mengen in und aus der Netzwerk-Bytereihenfolge wird eine Reihe von Konvertierungsroutinen bereitgestellt. Diese Routinen verwenden als Eingabeparameter das Sockethandle, dem eine [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) zugeordnet ist. Der **NetworkByteOrder-Member** der **WSAPROTOCOL \_ INFO-Struktur** gibt die gewünschte Netzwerkbytereihenfolge an (derzeit entweder Big-Endian oder Little-Endian).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Portieren von Socketanwendungen in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**WSAPROTOCOL-INFORMATIONEN \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
