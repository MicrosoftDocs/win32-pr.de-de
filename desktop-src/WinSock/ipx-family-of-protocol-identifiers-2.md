---
description: Der Protokollparameter in Socket und WSASocket ist ein Bezeichner, der einen Netzwerktyp und eine Methode zum Identifizieren der verschiedenen Transportprotokolle festlegt, die im Netzwerk ausgeführt werden.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: IPX-Familie von Protokollbezeichnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549e1dbdb9d379e87ed8e22871188b0b7762e924a695721f1c860fce14f2a2e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733650"
---
# <a name="ipx-family-of-protocol-identifiers"></a>IPX-Familie von Protokollbezeichnern

Der *Protokollparameter* in [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) und [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) ist ein Bezeichner, der einen Netzwerktyp und eine Methode zum Identifizieren der verschiedenen Transportprotokolle festlegt, die im Netzwerk ausgeführt werden. Im Gegensatz zu IP verwendet IPX keinen einzelnen Protokollwert für die Auswahl eines Transportstapels. Da es keine Netzwerkanforderung gibt, einen bestimmten Wert für jedes Transportprotokoll zu verwenden, können wir diese problemlos für Winsock-Anwendungen zuweisen. Wir vermeiden die Werte 0 bis 255, um Konflikte mit den entsprechenden PF \_ INET-Protokollwerten zu vermeiden.



| Name         | Wert       | Sockettypen              | Beschreibung                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| Reserviert     | 0 - 255       |                           | Reserviert für PF \_ INET-Protokollwerte.              |
| NSPROTO \_ IPX | 1000 - 1255 | SOCK \_ DGRAM SOCK \_ RAW     | Datagrammdienst für IPX.                           |
| NSPROTO \_ SPX | 1256        | SOCK \_ STREAM SOCK \_ SEQPKT | Zuverlässiger Paketaustausch mit Paketen fester Größe. |



 

> [!Note]  
> Wenn NSPROTO \_ SPX angegeben wird, wird das SPX II-Protokoll automatisch verwendet, wenn beide Endpunkte dazu in der Lage sind.

 

 

 



