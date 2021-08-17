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

Die Socketfreigabe zwischen Prozessen in Windows Sockets wird wie folgt implementiert. Ein Quellprozess ruft [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) auf, um eine spezielle [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) abzurufen. Dabei wird ein IPC-Mechanismus (Interprocess Communications) verwendet, um den Inhalt dieser Struktur an einen Zielprozess zu übergeben. Der Zielprozess verwendet dann die **WSAPROTOCOL \_ INFO-Struktur** in einem Aufruf von [**WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) Der von dieser Funktion zurückgegebene Socketdeskriptor ist ein zusätzlicher Socketdeskriptor für einen zugrunde liegenden Socket, der daher freigegeben wird.

Es liegt in der Verantwortung des Dienstanbieters, alle vorgänge auszuführen, die im Kontext des Quellprozesses erforderlich sind, und eine [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) zu erstellen, die erkannt wird, wenn sie anschließend als Parameter für [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) im Kontext der Zielprozesse angezeigt wird. Der **dwProviderReserved-Member** der **WSAPROTOCOL \_ INFO-Struktur** ist für die Verwendung durch den Dienstanbieter verfügbar und kann verwendet werden, um alle nützlichen Kontextinformationen zu speichern, einschließlich eines duplizierten Handles.

Dieser Mechanismus ist sowohl für Singlethreadversionen als auch präemptive Multithreadversionen von Windows geeignet. Beachten Sie jedoch, dass Sockets für Threads in einem bestimmten Prozess freigegeben werden können, ohne die [**WSPDuplicateSocket-Funktion**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) zu verwenden, da ein Socketdeskriptor in allen Threads eines Prozesses gültig ist.

Wie im Abschnitt [Deskriptorzuordnung](descriptor-allocation-2.md)beschrieben, müssen IFS-Anbieter beim Zuordnen neuer Socketdeskriptoren [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) und Nicht-IFS-Anbieter [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle)aufrufen.

Ein mögliches Szenario zum Einrichten und Verwenden eines freigegebenen Sockets in einem Übergabemodus ist in der folgenden Tabelle dargestellt.

| Quellprozess                                                                                                                          | IPC    | Zielprozess                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket), [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) Fordert den Zielprozessbezeichner an.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) Empfängt die Prozessbezeichneranforderung und antwortet.                          |
| 4) Empfängt den Prozessbezeichner.                                                                                                         | <== |                                                                               |
| 5) Ruft [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) auf, um eine spezielle [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) abzurufen. |        |                                                                               |
| 6) Sendet **die WSAPROTOCOL \_ INFO-Struktur** an das Ziel.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) Empfängt [**die WSAPROTOCOL \_ INFO-Struktur.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)        |
|                                                                                                                                         |        | 8) Ruft [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) auf, um einen freigegebenen Socketdeskriptor zu erstellen. |
|                                                                                                                                         |        | 9)Verwendet freigegebenen Socket für den Datenaustausch.                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
