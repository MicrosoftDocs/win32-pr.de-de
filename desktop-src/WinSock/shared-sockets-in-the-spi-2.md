---
description: Socketfreigabe in Windows Sockets (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Freigegebene Sockets in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0992768a7f3b38f27e4d40c54673e63e855687d0e9b9162e8b9e3cd1d1711d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559698"
---
# <a name="shared-sockets-in-the-spi"></a>Freigegebene Sockets in der SPI

Die Socketfreigabe zwischen Prozessen in Windows Sockets wird wie folgt implementiert. Ein Quellprozess ruft [**WSPDuplicateSocket auf,**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) um eine spezielle [**WSAPROTOCOL \_ INFO-Struktur zu**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) erhalten. Sie verwendet einen Mechanismus der prozessübergreifenden Kommunikation (Interprocess Communications, IPC), um den Inhalt dieser Struktur an einen Zielprozess zu übergeben. Der Zielprozess verwendet dann die **WSAPROTOCOL \_ INFO-Struktur** in einem Aufruf von [**WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) Der von dieser Funktion zurückgegebene Socketdeskriptor ist ein zusätzlicher Socketdeskriptor für einen zugrunde liegenden Socket, der somit freigegeben wird.

Der Dienstanbieter ist dafür verantwortlich, alle vorgänge durchzuführen, die im Quellprozesskontext erforderlich sind, und eine [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) zu erstellen, die erkannt wird, wenn sie anschließend als Parameter für [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) im Kontext der Zielprozesse angezeigt wird. Das **dwProviderReserved-Member** der **WSAPROTOCOL \_ INFO-Struktur** ist für die Verwendung durch den Dienstanbieter verfügbar und kann zum Speichern nützlicher Kontextinformationen verwendet werden, einschließlich eines duplizierten Handles.

Dieser Mechanismus ist sowohl für Singlethreadversionen als auch für präemptive Multithreadversionen von Windows. Beachten Sie jedoch, dass Sockets unter Threads in einem bestimmten Prozess freigegeben werden können, ohne die [**WSPDuplicateSocket-Funktion**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) zu verwenden, da ein Socketdeskriptor in allen Threads eines Prozesses gültig ist.

Wie im Abschnitt [Deskriptorzuordnung](descriptor-allocation-2.md)beschrieben, müssen IFS-Anbieter [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) aufrufen, wenn neue Socketdeskriptoren zugeordnet werden, und Nicht-IFS-Anbieter [**müssen WPUCreateSocketHandle aufrufen.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle)

Ein mögliches Szenario für die Einrichtung und Verwendung eines freigegebenen Sockets in einem Übergabemodus ist in der folgenden Tabelle dargestellt.

| Quellprozess                                                                                                                          | IPC    | Zielprozess                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) Fordert den Zielprozessbezeichner an.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) Empfängt die Prozessbezeichneranforderung und antwortet.                          |
| 4) Empfängt den Prozessbezeichner.                                                                                                         | <== |                                                                               |
| 5) Ruft [**WSPDuplicateSocket auf,**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) um eine spezielle [**WSAPROTOCOL \_ INFO-Struktur zu**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) erhalten. |        |                                                                               |
| 6) Sendet **die WSAPROTOCOL \_ INFO-Struktur** an das Ziel.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) Empfängt [**die WSAPROTOCOL \_ INFO-Struktur.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)        |
|                                                                                                                                         |        | 8) Ruft [**WSPSocket auf, um**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) einen freigegebenen Socketdeskriptor zu erstellen. |
|                                                                                                                                         |        | 9)Verwendet freigegebenen Socket für den Datenaustausch.                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
