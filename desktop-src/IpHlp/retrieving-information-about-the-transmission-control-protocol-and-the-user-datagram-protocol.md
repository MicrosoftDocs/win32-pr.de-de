---
description: IP-Hilfsobjekte ermöglichen den Zugriff auf Informationen zu Netzwerkprotokollen, die auf dem lokalen Computer verwendet werden.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Abrufen von Informationen über das Transmission Control-Protokoll und das User Datagram-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760843"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Abrufen von Informationen über das Transmission Control-Protokoll und das User Datagram-Protokoll

IP-Hilfsobjekte ermöglichen den Zugriff auf Informationen zu Netzwerkprotokollen, die auf dem lokalen Computer verwendet werden. Verwenden Sie die Funktionen, die in den folgenden Abschnitten beschrieben werden, um Informationen über das Transmission Control Protocol (TCP) und das User Datagram-Protokoll (UDP) auf dem lokalen Computer abzurufen.

Die [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) -Funktion Ruft die aktuellen Statistiken für TCP ab. Codebeispiele, die **GetTcpStatistics** betreffen, finden [Sie unter Abrufen von Informationen mithilfe von GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).

Die [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) -Funktion Ruft die aktuellen Statistiken für UDP ab.

Die [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) -Funktion Ruft die TCP-Verbindungstabelle ab. Die [**getudptable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) Ruft die UDP-listenertabelle ab.

Mithilfe der [**settcpentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) -Funktion kann ein Entwickler den Zustand einer angegebenen TCP-Verbindung auf den MIB- \_ TCP- \_ Status \_ Delete \_ TCB festlegen.

 

 



