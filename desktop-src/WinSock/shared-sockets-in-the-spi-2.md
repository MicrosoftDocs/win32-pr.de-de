---
description: Socketfreigabe in Windows Sockets (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Freigegebene Sockets in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ff0d8f73d2bd9de942d17de7f9564158d1810c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864039"
---
# <a name="shared-sockets-in-the-spi"></a>Freigegebene Sockets in der SPI

Die socketfreigabe zwischen Prozessen in Windows Sockets wird wie folgt implementiert. Von einem Quell Prozess wird [**wspdupliplatesocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) aufgerufen, um eine spezielle [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur zu erhalten. Er verwendet einen gewissen Prozess für die prozessübergreifende Kommunikation (IPC), um den Inhalt dieser Struktur an einen Ziel Prozess zu übergeben. Der Ziel Prozess verwendet dann die **wsaprotocol- \_ Informations** Struktur in einem [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)-aufrufsvorgang. Der von dieser Funktion zurückgegebene socketdeskriptor ist ein zusätzlicher socketdeskriptor für einen zugrunde liegenden Socket, der freigegeben wird.

Der Dienstanbieter ist dafür verantwortlich, alle Vorgänge auszuführen, die im Quell Prozess Kontext erforderlich sind, und eine [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur zu erstellen, die erkannt wird, wenn Sie anschließend als Parameter für [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) im Kontext der Ziel Prozesse angezeigt wird. Der **dwproviderreserved** -Member der **wsaprotocol- \_ Informations** Struktur ist für die Verwendung durch den Dienstanbieter verfügbar und kann verwendet werden, um nützliche Kontextinformationen, einschließlich eines doppelten Handles, zu speichern.

Dieser Mechanismus ist so konzipiert, dass er sowohl für Single Thread-als auch für präemptiv Versionen von Windows geeignet ist. Beachten Sie jedoch, dass Sockets in einem bestimmten Prozess unabhängig von den Threads gemeinsam genutzt werden können, ohne die [**wspduplithuesocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) -Funktion zu verwenden, da ein socketdeskriptor in allen Threads eines Prozesses gültig ist.

Wie im Abschnitt [deskriptorallocation](descriptor-allocation-2.md)beschrieben, müssen IFS-Anbieter, wenn neue socketdeskriptoren zugeordnet sind, [**wpumodifyifshandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) aufrufen, und nicht-IFS-Anbieter müssen [**wpukreatesockethandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle)aufrufen.

Ein mögliches Szenario für das Einrichten und Verwenden eines freigegebenen Sockets in einem Übergabe-Modus ist in der folgenden Tabelle dargestellt.

| Quellprozess                                                                                                                          | IPC    | Zielprozess                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket), [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) Anforderungen an den Ziel Prozess Bezeichner.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) empfängt die prozessbezeichneranforderung und antwortet.                          |
| 4) empfängt Prozess Bezeichner.                                                                                                         | <== |                                                                               |
| 5) ruft [**wspduplialisiesocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) auf, um eine spezielle [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur zu erhalten. |        |                                                                               |
| 6) sendet die **wsaprotocol- \_ Informations** Struktur an das Ziel.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) empfängt die [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur.        |
|                                                                                                                                         |        | 8) ruft [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) auf, um einen freigegebenen socketdeskriptor zu erstellen. |
|                                                                                                                                         |        | 9) verwendet freigegebenen Socket für den Datenaustausch.                                       |
| 10) [ **wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
