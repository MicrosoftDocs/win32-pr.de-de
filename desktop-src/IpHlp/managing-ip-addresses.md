---
description: Das IP-Hilfsprogramm kann bei der Verwaltung von IP-Adressen helfen, die Schnittstellen auf dem lokalen Computer zugeordnet sind. Verwenden Sie die in den folgenden Abschnitten beschriebenen Funktionen für die IP-Adressverwaltung.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Verwalten von IP-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51e0e1e30adf064330a2a4070e6872ca87b50b94e3ad1ab458c3c84878d5549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560320"
---
# <a name="managing-ip-addresses"></a>Verwalten von IP-Adressen

Das IP-Hilfsprogramm kann bei der Verwaltung von IP-Adressen helfen, die Schnittstellen auf dem lokalen Computer zugeordnet sind. Verwenden Sie die in den folgenden Abschnitten beschriebenen Funktionen für die IP-Adressverwaltung.

Die [**GetIpAddrTable-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) ruft eine Tabelle ab, die die Zuordnung von IP-Adressen zu Schnittstellen enthält. Mehrere IP-Adressen können derselben Schnittstelle zugeordnet sein.

Verwenden Sie [**die AddIPAddress-Funktion,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) um einer bestimmten Schnittstelle eine IP-Adresse hinzuzufügen. Verwenden Sie die [**DeleteIPAddress-Funktion,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) um IP-Adressen zu entfernen, die zuvor mit **AddIPAddress** hinzugefügt wurden.

Die [**Funktionen IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) und [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) erfordern, dass der lokale Computer dhcp (Dynamic Host Configuration Protocol) verwendet. Die **IpReleaseAddress-Funktion** gibt eine IP-Adresse frei, die zuvor von DHCP erhalten wurde. Die **IpRenewAddress-Funktion** erneuert eine DHCP-Lease für eine bestimmte IP-Adresse. Eine DHCP-Lease ermöglicht es einem Computer, eine IP-Adresse für einen bestimmten Zeitraum zu verwenden.

-   Codebeispiele im Zusammenhang [**mit GetIpAddrTable finden**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) Sie unter [Verwalten von IP-Adressen mit GetIpAddrTable.](managing-ip-addresses-using-getipaddrtable.md)

-   Codebeispiele für [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) und [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)finden Sie unter Verwalten von IP-Adressen mit [AddIPAddress und DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Codebeispiele für [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) und [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) finden Sie unter Verwalten von [DHCP-Leases mit ipReleaseAddress und IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 



