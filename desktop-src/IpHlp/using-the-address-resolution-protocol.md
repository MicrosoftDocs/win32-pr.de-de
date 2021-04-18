---
description: Sie können das IP-Hilfsprogramm verwenden, um ARP-Vorgänge (Address Resolution Protocol) für den lokalen Computer auszuführen. Verwenden Sie die folgenden Funktionen, um die ARP-Tabelle abzurufen und zu ändern.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Verwenden des adressauflösungsprotokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350917"
---
# <a name="using-the-address-resolution-protocol"></a>Verwenden des adressauflösungsprotokolls

Sie können das IP-Hilfsprogramm verwenden, um ARP-Vorgänge (Address Resolution Protocol) für den lokalen Computer auszuführen. Verwenden Sie die folgenden Funktionen, um die ARP-Tabelle abzurufen und zu ändern.

Die [**getipnetttabelle**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) Ruft die ARP-Tabelle ab. Die ARP-Tabelle enthält die Zuordnung von IP-Adressen zu physischen Adressen. Physische Adressen werden manchmal auch als Mac-Adressen (Media Access Controller) bezeichnet.

Verwenden Sie die Funktionen " [**forateipnetentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) " und " [**deleteipnetentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) ", um der Tabelle bestimmte ARP-Einträge hinzuzufügen oder daraus zu entfernen. Die [**flushipnettfunktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) löscht alle Einträge aus der Tabelle.

Um Proxy-ARP-Einträge zu erstellen oder zu löschen, verwenden Sie die Funktionen " [**forateproxyarpentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) " und " [**deleteproxyarpentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) ".

Die [**sendarp**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) -Funktion sendet eine ARP-Anforderung an das lokale Netzwerk.

 

 



