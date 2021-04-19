---
description: IP-Hilfsobjekte können bei der Verwaltung von IP-Adressen helfen, die Schnittstellen auf dem lokalen Computer zugeordnet sind Verwenden Sie die Funktionen, die in den folgenden Abschnitten für die IP-Adressverwaltung beschrieben werden.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Verwalten von IP-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356736"
---
# <a name="managing-ip-addresses"></a>Verwalten von IP-Adressen

IP-Hilfsobjekte können bei der Verwaltung von IP-Adressen helfen, die Schnittstellen auf dem lokalen Computer zugeordnet sind Verwenden Sie die Funktionen, die in den folgenden Abschnitten für die IP-Adressverwaltung beschrieben werden.

Die [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) -Funktion Ruft eine Tabelle ab, die die Zuordnung von IP-Adressen zu Schnittstellen enthält. Der gleichen Schnittstelle können mehr als eine IP-Adresse zugeordnet werden.

Verwenden Sie die [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) -Funktion, um einer bestimmten Schnittstelle eine IP-Adresse hinzuzufügen. Verwenden Sie zum Entfernen von IP-Adressen, die zuvor mit **addipaddress** hinzugefügt wurden, die [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion.

Die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion und die [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion erfordern, dass der lokale Computer DHCP (Dynamic Host Configuration Protocol) verwendet. Die **ipreleaseaddress** -Funktion gibt eine IP-Adresse frei, die zuvor von DHCP abgerufen wurde. Die **iprenewaddress** -Funktion erneuert eine DHCP-Lease für eine bestimmte IP-Adresse. Eine DHCP-Lease ermöglicht es einem Computer, eine IP-Adresse für einen bestimmten Zeitraum zu verwenden.

-   Codebeispiele, die [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) betreffen, finden [Sie unter Verwalten von IP-Adressen mit getipaddrtable](managing-ip-addresses-using-getipaddrtable.md).

-   Codebeispiele, die [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) und [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)betreffen, finden [Sie unter Verwalten von IP-Adressen mit addipaddress und deleteipaddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Codebeispiele, die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) und [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) betreffen, finden [Sie unter Verwalten von DHCP-Leases mithilfe von ipreleaseaddress und iprenewaddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 



