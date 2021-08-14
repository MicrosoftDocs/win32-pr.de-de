---
title: Verwenden von Teredo mit ip helper
description: Die IP-Hilfs-API (Internet Protocol Helper) wird von einer Anwendung verwendet, um wichtige Informationen zur Netzwerkkonfiguration des lokalen Computers zu sammeln und bereitzustellen.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e977dd585f9759a4eef93daca55e0ff95abdc98085393577afabb4ae6e5908ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990800"
---
# <a name="using-teredo-with-ip-helper"></a>Verwenden von Teredo mit ip helper

Die IP-Hilfssoftware-API [(Internet Protocol Helper)](/windows/desktop/IpHlp/about-ip-helper) wird von einer Anwendung verwendet, um wichtige Informationen zur Netzwerkkonfiguration des lokalen Computers zu sammeln und bereitzustellen. Beim Betrieb auf der Windows Vista-Plattform umfassen diese Informationen den dynamischen UDP-Port, der der Teredo-Schnittstelle zugewiesen ist, und Änderungen, die am angegebenen Port auftreten können.

Die folgenden Funktionen werden von der IP-Hilfs-API verwendet, um die Verwendung der Teredo-Schnittstelle zu vereinfachen:

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 