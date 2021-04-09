---
description: IP-Hilfsobjekte bieten Informations Abruf Funktionen, die für die Netzwerkverwaltung des lokalen Computers nützlich sind.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Abrufen von Informationen über das Internetprotokoll und das Internet Control Message-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958681"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a>Abrufen von Informationen über das Internetprotokoll und das Internet Control Message-Protokoll

IP-Hilfsobjekte bieten Informations Abruf Funktionen, die für die Netzwerkverwaltung des lokalen Computers nützlich sind. Die folgenden Funktionen rufen Statistiken für das Internetprotokoll (IP) und das Internet Control Message-Protokoll (ICMP) ab. Sie können diese Funktionen auch verwenden, um bestimmte Konfigurationsparameter für IP festzulegen.

Die [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) -Funktion Ruft die aktuellen IP-Statistiken für den lokalen Computer ab. Codebeispiele mit **GetIpStatistics** finden [Sie unter Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md).

Die [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) -Funktion Ruft die aktuellen ICMP-Statistiken ab.

Verwenden Sie [**die Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) "Funktion", um die IP-Weiterleitung zu aktivieren oder zu deaktivieren Mit dieser Funktion können Sie auch die Standard Gültigkeitsdauer (Time-to-Live, TTL) für IP-Datagramme festlegen. Alternativ können Sie die Gültigkeitsdauer mithilfe der Funktion " [**setipttl**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) " festlegen.

 

 



