---
description: Es muss immer darauf achten, unterschiede zwischen der Byte reihenfolge, die zum Speichern von ganzen Zahlen durch die Hostarchitektur verwendet wird, und der byte-Reihenfolge zu berücksichtigen, die von einzelnen Transportprotokollen im Netzwerk verwendet wird.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: Bytereihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554b9f00b67fcd602daee0ed33443e228e4e3976f334506d949e3af79fef7e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560180"
---
# <a name="byte-ordering"></a>Bytereihenfolge

Es muss immer darauf achten, unterschiede zwischen der Byte reihenfolge, die zum Speichern von ganzen Zahlen durch die Hostarchitektur verwendet wird, und der byte-Reihenfolge zu berücksichtigen, die von einzelnen Transportprotokollen im Netzwerk verwendet wird. Jeder Verweis auf eine Adresse oder Portnummer, die an oder von einer Windows Sockets-Routine übergeben wird, muss in der Netzwerk reihenfolge (Big-Endian) für das verwendete Protokoll sein. Im Fall von IP umfasst dies die IP-Adresse und die Portparameter einer [**Sockaddr-Struktur**](sockaddr-2.md) (aber nicht den *Parameter sin \_ family).*

Eine Reihe von UNIX-Systemen arbeiten mit CPUs, die ganze Zahlen in der Netzwerk-Byte-Reihenfolge (Big-Endian) darstellen. Daher kann die Notwendigkeit, ganze Zahlen von der Host-Byte-Reihenfolge in die Netzwerk-Byte reihenfolge zu konvertieren, ignoriert werden, ohne Probleme zu verursachen, auch wenn dies aus Portabilitäts-Grund nicht empfohlen wird.

Im Gegensatz dazu ist die Byte reihenfolge, die verwendet wird, um ganze Zahlen von den meisten Intel® CPUs zu darstellen, little-endian. Daher ist es zwingend erforderlich, ganze Zahlen von der Byte reihenfolge des Hosts in die Netzwerk-Byte reihenfolge zu konvertieren, bevor sie in Winsock Sockets-Funktionen und -Strukturen verwendet werden.

Stellen Sie sich eine Anwendung vor, die normalerweise einen Server über den TCP-Port kontaktiert, der dem Zeitdienst entspricht, aber einen Mechanismus für den Benutzer bietet, um einen alternativen Port anzugeben. Die von [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) zurückgegebene Portnummer befindet sich bereits in der Netzwerk reihenfolge. Dies ist das Format, das zum Erstellen einer Adresse erforderlich ist, sodass keine Übersetzung erforderlich ist. Wenn der Benutzer jedoch einen anderen Port verwendet, der als ganze Zahl eingegeben wird, muss die Anwendung dies vom Host in die TCP/IP-Netzwerk reihenfolge konvertieren (mithilfe der [**htons-**](/windows/desktop/api/winsock/nf-winsock-htons) oder [**WSAHtons-Funktion),**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) bevor es zum Erstellen einer Adresse verwendet wird. Wenn die Anwendung hingegen die Nummer des Ports innerhalb einer Adresse anzeigen würde (z. B. von [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) zurückgegeben), muss die Portnummer von der Netzwerk- in die Host reihenfolge konvertiert werden (mithilfe der [**ntohs-**](/windows/desktop/api/winsock/nf-winsock-ntohs) oder [**WSANtohs-Funktion),**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) bevor sie angezeigt werden kann.

Da sich die Bytebestellungen von Intel und internet unterscheiden, sind die oben beschriebenen Konvertierungen unvermeidbar. Anwendungsautoren werden darauf gewarnunget, dass sie die im Rahmen von Winsock bereitgestellten Standardkonvertierungsfunktionen verwenden sollten, anstatt ihren eigenen Konvertierungscode zu schreiben, da zukünftige Implementierungen von Winsock wahrscheinlich auf Systemen ausgeführt werden, deren Host reihenfolge mit der Netzwerk-Byte reihenfolge identisch ist. Nur Anwendungen, die die Standardkonvertierungsfunktionen zwischen Host- und Netzwerk-Byte reihenfolge verwenden, sind wahrscheinlich portabel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**nt durch**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Portieren von Socketanwendungen zu Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**sockaddr**](sockaddr-2.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtetter**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



