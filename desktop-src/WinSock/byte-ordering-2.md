---
description: Es muss stets darauf geachtet werden, dass Unterschiede zwischen der Byte Reihenfolge, die zum Speichern ganzer Zahlen in der Host Architektur verwendet wird, und der Byte-Reihenfolge, die von einzelnen Transportprotokollen verwendet wird, berücksichtigt werden.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: Bytereihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484955"
---
# <a name="byte-ordering"></a>Bytereihenfolge

Es muss stets darauf geachtet werden, dass Unterschiede zwischen der Byte Reihenfolge, die zum Speichern ganzer Zahlen in der Host Architektur verwendet wird, und der Byte-Reihenfolge, die von einzelnen Transportprotokollen verwendet wird, berücksichtigt werden. Alle Verweise auf eine Adresse oder eine Portnummer, die an eine oder von einer Windows Sockets-Routine übergeben wird, müssen sich in der Netzwerk Reihenfolge (Big-enumdian) für das verwendete Protokoll befinden. Im Fall von IP umfasst dies die IP-Adresse und die Port Parameter einer [**sockaddr**](sockaddr-2.md) -Struktur (aber nicht den *Sin- \_ Family* -Parameter).

Eine Reihe von UNIX-Systemen funktioniert mit CPUs, die ganze Zahlen in der Netzwerk-Byte Reihenfolge (Big-Endian) darstellen. Daher kann die Notwendigkeit, ganze Zahlen von der Host-Byte Reihenfolge in die Netzwerk-Byte Reihenfolge zu konvertieren, ignoriert werden, auch wenn dies für die Portabilität nicht empfehlenswert ist.

Im Gegensatz dazu ist die Byte-Reihenfolge, die zur Darstellung ganzer Zahlen für die meisten Intel® CPUs verwendet wird, Little-Endian. Daher ist es obligatorisch, dass ganze Zahlen von der Host-Byte Reihenfolge in die Netzwerk-Byte Reihenfolge konvertiert werden, bevor Sie in Winsock Sockets-Funktionen und-Strukturen verwendet werden

Stellen Sie sich eine Anwendung vor, die normalerweise einen Server auf dem TCP-Port kontaktiert, der dem Zeit Dienst entspricht, aber einen Mechanismus bereitstellt, mit dem der Benutzer einen alternativen Port angeben kann. Die von [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) zurückgegebene Portnummer ist bereits in der Netzwerk Reihenfolge vorhanden. Dies ist das Format, das zum Erstellen einer Adresse erforderlich ist, sodass keine Übersetzung erforderlich ist. Wenn sich der Benutzer jedoch [**für die Verwendung**](/windows/desktop/api/winsock/nf-winsock-htons) eines anderen Ports entscheidet, der als Ganzzahl eingegeben wird, muss die Anwendung diese in eine TCP/IP-Netzwerk Reihenfolge konvertieren, bevor [](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) Sie zum Erstellen einer Adresse verwendet wird. Wenn im Gegensatz dazu die Anwendung die Nummer des Ports innerhalb einer Adresse anzeigen soll (z. b. von [**getPeer Name**](/windows/desktop/api/winsock/nf-winsock-getpeername) ), muss die Portnummer aus dem Netzwerk in die Host Reihenfolge (mithilfe der [**ndehs**](/windows/desktop/api/winsock/nf-winsock-ntohs) -oder [**wsandehs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) -Funktion) konvertiert werden, bevor Sie angezeigt werden kann.

Da sich die Intel-und Internet-Byte Bestellungen unterscheiden, sind die in der obigen beschriebenen Konvertierungen unvermeidlich. Anwendungs Schreiber werden gewarnt, dass Sie die Standard Konvertierungs Funktionen verwenden sollten, die als Teil von Winsock bereitgestellt werden, anstatt ihren eigenen Konvertierungs Code zu schreiben, da zukünftige Implementierungen von Winsock wahrscheinlich auf Systemen ausgeführt werden, für die die Host Reihenfolge mit der Netzwerk-Byte Reihenfolge identisch ist. Nur Anwendungen, die die Standard Konvertierungs Funktionen zwischen der Host-und der Netzwerk-Byte Reihenfolge verwenden, sind wahrscheinlich portabel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**getPeer Name**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

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

[**sockaddr**](sockaddr-2.md)
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
</dt> </dl>

 

 



