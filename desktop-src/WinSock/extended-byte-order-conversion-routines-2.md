---
description: Windows Sockets 2 geht nicht davon aus, dass die Netzwerk-Byte Reihenfolge für alle Protokolle identisch ist.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Erweiterte Byte-Order Konvertierungs Routinen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526183"
---
# <a name="extended-byte-order-conversion-routines"></a>Erweiterte Byte-Order Konvertierungs Routinen

Windows Sockets 2 geht nicht davon aus, dass die Netzwerk-Byte Reihenfolge für alle Protokolle identisch ist. Eine Reihe von Konvertierungs Routinen wird zum Konvertieren von 16-Bit-und 32-Bit-Mengen in und aus der Netzwerk-Byte Reihenfolge bereitgestellt. Diese Routinen akzeptieren als Eingabeparameter das Sockethandle, dem eine [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur zugeordnet ist. Der **networkbyteorder** -Member der **wsaprotocol- \_ Informations** Struktur gibt die gewünschte netzwerkbyte Reihenfolge an (zurzeit Big-Endian oder Little-Endian).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htonnen**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**nzu HLS**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**NUM**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> <dt>

[**Wsahtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**Wsahtonnen**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**Wsanum**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**Wsanum**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**wsaprotocol- \_ Informationen**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
