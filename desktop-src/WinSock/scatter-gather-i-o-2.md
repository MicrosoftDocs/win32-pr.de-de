---
description: Die Funktionen "WSARecv", "WSARecvFrom", "wsarecvmsg", "wsasend", "wsasendmsg" und "WSASendTo" nehmen ein Array von Anwendungs Puffern als Eingabeparameter an und können für die e/a-Vorgänge vom Typ "Scatter/Gather" (oder "VEC
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: Scatter/Gather-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355641"
---
# <a name="scattergather-io"></a>Scatter/Gather-e/a

Die Funktionen " [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)", " [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)", " [**LPFN_WSARECVMSG" (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), " [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)", " [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)" und " [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) " nehmen ein Array von Anwendungs Puffern als Eingabeparameter an und können für die e/a-Vorgänge für Punkt/Erfassung (oder Vektoren) verwendet werden Dies kann sehr nützlich sein, wenn Teile jeder übermittelten Nachricht zusätzlich zum Nachrichtentext aus einer oder mehreren Header Komponenten fester Länge bestehen. Diese Header Komponenten müssen von der Anwendung nicht in einem einzelnen zusammenhängenden Puffer vor dem Senden verkettet werden. Beim Empfang von können die Header Komponenten automatisch in separate Puffer aufgeteilt werden, sodass der Nachrichtentext selbst nicht mehr angezeigt wird.

Beim Empfang in mehrere Puffer erfolgt der Abschluss, wenn Daten aus dem Netzwerk eintreffen, unabhängig davon, ob alle angegebenen Puffer verwendet werden.

 

 
