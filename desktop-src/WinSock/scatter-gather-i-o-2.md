---
description: Die Funktionen WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg und WSASendTo nehmen alle ein Array von Anwendungspuffern als Eingabeparameter an und können für Punkt-/Gather-E/A(oder vektorierte) E/A verwendet werden.
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: Punkt-/Sammeln-E/A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4dc580065655c2d69485a49cd41919345c566c32ec2ff9cd1055383853c7438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794680"
---
# <a name="scattergather-io"></a>Punkt-/Sammeln-E/A

Die Funktionen [**WSARecv,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**WSARecvFrom,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) [**LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)und [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) nehmen alle ein Array von Anwendungspuffern als Eingabeparameter an und können für Punkt-/Gather-E/A(oder vektorierte) E/A verwendet werden. Dies kann in Fällen sehr nützlich sein, in denen Teile jeder zu übertragenden Nachricht zusätzlich zum Nachrichtentext aus einer oder mehreren Headerkomponenten fester Länge bestehen. Solche Headerkomponenten müssen von der Anwendung vor dem Senden nicht zu einem einzelnen zusammenhängenden Puffer verkettet werden. Ebenso können die Headerkomponenten beim Empfang automatisch in separate Puffer aufgeteilt werden, und der Nachrichtentext selbst wird verlassen.

Beim Empfang in mehreren Puffern erfolgt die Vervollständigung, wenn Daten aus dem Netzwerk eintreffen, unabhängig davon, ob alle bereitgestellten Puffer verwendet werden.

 

 
