---
description: Es gibt mehrere socketattribute, die über den flags-Parameter in wspsocket angegeben werden können.
ms.assetid: 5fd4321b-a5cc-4921-bec5-bdf625261ea2
title: Socketattributflags und-Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da1a5f621a7d9f489f4e91782462c215659772b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355294"
---
# <a name="socket-attribute-flags-and-modes"></a>Socketattributflags und-Modi

Es gibt mehrere socketattribute, die über den *Flags* -Parameter in [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)angegeben werden können. Das überlappende Flag für das WSA- \_ Flag \_ gibt an, dass ein Socket für überlappende e/a-Vorgänge verwendet wird. Die Unterstützung dieses Attributs ist für alle Dienstanbieter obligatorisch. Weitere Informationen finden Sie unter überlappende e [/](overlapped-i-o-2.md) a. Beachten Sie, dass das Erstellen eines Sockets mit dem überlappenden Attribut keine Auswirkung darauf hat, ob sich ein Socket derzeit im blockierenden oder nicht blockierenden Modus befindet. Sockets, die mit dem überlappenden Attribut erstellt wurden, können verwendet werden, um überlappende e/a auszuführen, und dadurch wird der Blockierungs Modus eines Sockets nicht geändert. Da überlappende e/a-Vorgänge nicht blockiert werden, ist der Blockierungs Modus eines Sockets für diese Vorgänge irrelevant.

Beim Erstellen von Sockets, die für Multipoint-und/oder Multicast Vorgänge verwendet werden sollen, werden vier zusätzliche Attributflags verwendet, und die Unterstützung für diese Attribute ist optional. Anbieter, die Multipoint-Attribute unterstützen, geben dies über das \_ Multipoint-Bit XP1 Suppport \_ in den jeweiligen [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Strukturen an. Die Definition und Verwendung der einzelnen Flags finden Sie unter [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) und [Protokoll unabhängige Multicast-und Multipoint-APIs in der API](protocol-independent-multicast-and-multipoint-in-the-spi-2.md) . Nur Sockets, die mit Multipoint-bezogenen Attributen erstellt werden, können in der [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) -Funktion zum Erstellen von Multipoint-Sitzungen verwendet werden.

Ein Socket befindet sich jederzeit in einem von zwei Modi: Blockierung und nicht Blockierung. Sockets werden standardmäßig im blockierenden Modus erstellt und können in den nicht blockierenden Modus geändert werden, indem [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), [**wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))oder [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))aufgerufen wird. Ein Socket kann mithilfe von **wspioctl** wieder in den Blockierungs Modus gewechselt werden, wenn " **wspasyncselect** " oder " **wspeventselect** " nicht aktiv ist. Der Modus für einen Socket wirkt sich nur auf die Funktionen aus, die blockiert werden können, und wirkt sich nicht auf überlappende e/a-Vorgänge aus. Weitere Informationen finden Sie unter [Blockieren von Vorgängen](blocking-operations-2.md) .

 

 
