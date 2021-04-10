---
description: Der Protokoll Parameter in Socket und wsasocket ist ein Bezeichner, der einen Netzwerktyp und eine Methode zum Identifizieren der verschiedenen Transportprotokolle festlegt, die im Netzwerk ausgeführt werden.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: IPX-Familie von Protokoll bezeichlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129165"
---
# <a name="ipx-family-of-protocol-identifiers"></a>IPX-Familie von Protokoll bezeichlern

Der *Protokoll* Parameter in [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) und [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) ist ein Bezeichner, der einen Netzwerktyp und eine Methode zum Identifizieren der verschiedenen Transportprotokolle festlegt, die im Netzwerk ausgeführt werden. Anders als bei IP verwendet IPX keinen einzelnen Protokoll Wert für die Auswahl eines Transport Stapels. Da es keine Netzwerk Anforderung gibt, einen bestimmten Wert für jedes Transportprotokoll zu verwenden, können wir diese auf eine Weise zuweisen, die für Winsock-Anwendungen geeignet ist. Wir vermeiden Werte 0 – 255, um Konflikte mit den entsprechenden PF- \_ inet-Protokoll Werten zu vermeiden.



| Name         | Wert       | Sockettypen              | BESCHREIBUNG                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| Reserviert     | 0 - 255       |                           | Reserviert für PF- \_ inet-Protokoll Werte.              |
| nsproto- \_ IPX | 1000-1255 | sock- \_ dgram Sock- \_ Rohdaten     | Datagramm-Dienst für IPX.                           |
| nsproto- \_ SPX | 1256        | sock-Datenstrom (sock) \_ \_ | Zuverlässiger Paket Austausch mithilfe von Paketen mit fester Größe. |



 

> [!Note]  
> Wenn nsproto \_ SPX angegeben ist, wird das SPX II-Protokoll automatisch verwendet, wenn beide Endpunkte dies tun können.

 

 

 



