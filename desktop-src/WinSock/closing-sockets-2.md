---
description: Wspclosesocket gibt den socketdeskriptor frei, sodass alle ausstehenden Vorgänge in allen Threads desselben Prozesses abgebrochen werden, und jeder weitere Verweis darauf schlägt fehl.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Schließen von Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d0c877767925f67e07427a77dc8ec8445f30c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526189"
---
# <a name="closing-sockets"></a>Schließen von Sockets

[**Wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) gibt den socketdeskriptor frei, sodass alle ausstehenden Vorgänge in allen Threads desselben Prozesses abgebrochen werden, und jeder weitere Verweis darauf schlägt fehl. Beachten Sie, dass ein Verweis Zähler für freigegebene Sockets verwendet werden sollte. wenn es sich hierbei um den letzten Verweis auf einen zugrunde liegenden Socket handelt, sollten die diesem Socket zugeordneten Informationen verworfen werden, wenn ein ordnungsgemäßes schließen nicht angefordert wird (d. h., dass \_ DontLinger nicht festgelegt ist). Im Fall der \_ Festlegung von DontLinger werden alle Daten, die für die Übertragung in die Warteschlange eingereiht werden, nach Möglichkeit gesendet, bevor dem Socket zugeordnete Informationen freigegeben werden. Weitere Informationen finden Sie unter **wspclosesocket** .

Für nonifs-Dienstanbieter muss [**wpuclosesockethandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) aufgerufen werden, um den Sockethandle zurück zur Windows Sockets 2-dll freizugeben.

 

 
