---
description: Sie können das IP-Hilfsprogramm verwenden, um ARP-Vorgänge (Address Resolution Protocol) für den lokalen Computer durchzuführen. Verwenden Sie die folgenden Funktionen, um die ARP-Tabelle abzurufen und zu ändern.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Verwenden des Adressauflösungsprotokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca1ef7e5d657476ff85a8893d71e197a034c70234e44f32317b7b05f58c9b94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290010"
---
# <a name="using-the-address-resolution-protocol"></a>Verwenden des Adressauflösungsprotokolls

Sie können das IP-Hilfsprogramm verwenden, um ARP-Vorgänge (Address Resolution Protocol) für den lokalen Computer durchzuführen. Verwenden Sie die folgenden Funktionen, um die ARP-Tabelle abzurufen und zu ändern.

Die [**GetIpNetTable ruft**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) die ARP-Tabelle ab. Die ARP-Tabelle enthält die Zuordnung von IP-Adressen zu physischen Adressen. Physische Adressen werden manchmal als MAC-Adressen (Media Access Controller) bezeichnet.

Verwenden Sie [**die Funktionen CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) und [**DeleteIpNetEntry,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) um der Tabelle bestimmte ARP-Einträge hinzuzufügen oder daraus zu entfernen. Die [**FlushIpNetTable-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) löscht alle Einträge aus der Tabelle.

Verwenden Sie zum Erstellen oder Löschen von Proxy-ARP-Einträgen die [**Funktionen CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) und [**DeleteProxyArpEntry.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry)

Die [**SendARP-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) sendet eine ARP-Anforderung an das lokale Netzwerk.

 

 



