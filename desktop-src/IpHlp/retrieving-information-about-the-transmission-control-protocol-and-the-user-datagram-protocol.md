---
description: Das IP-Hilf hilft ihnen, auf Informationen zu Netzwerkprotokollen zuzugreifen, die auf dem lokalen Computer verwendet werden.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Abrufen von Informationen über das Transmission Control-Protokoll und das User Datagram-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f10691c39e1f1a2c9c92af8736549427f01cc2400773e214f3a4d5f536fa46e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102050"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a>Abrufen von Informationen über das Transmission Control-Protokoll und das User Datagram-Protokoll

Das IP-Hilf hilft ihnen, auf Informationen zu Netzwerkprotokollen zuzugreifen, die auf dem lokalen Computer verwendet werden. Verwenden Sie die in den folgenden Absätzen beschriebenen Funktionen, um Informationen über tcp (Transmission Control Protocol) und das User Datagram Protocol (UDP) auf dem lokalen Computer abzurufen.

Die [**GetTcpStatistics-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) ruft die aktuelle Statistik für TCP ab. Codebeispiele für **GetTcpStatistics** finden Sie unter [Abrufen von Informationen mit getTcpStatistics.](retrieving-information-using-gettcpstatistics.md)

Die [**GetUdpStatistics-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) ruft die aktuelle Statistik für UDP ab.

Die [**GetTcpTable-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) ruft die TCP-Verbindungstabelle ab. Die [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) ruft die UDP-Listenertabelle ab.

Mit der [**SetTcpEntry-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) kann ein Entwickler den Status einer angegebenen TCP-Verbindung auf MIB \_ TCP STATE DELETE \_ \_ \_ TCB festlegen.

 

 



