---
description: DNS-Namen bestehen aus einer oder mehreren Komponenten, die durch einen Punkt getrennt sind (z. B. msdn.microsoft.com).
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: Computernamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8687d6d510247a2bbb2850e6a668a63f0108b2bc344ed161cb73e28d2b47eeaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885790"
---
# <a name="computer-names"></a>Computernamen

DNS-Namen bestehen aus einer oder mehreren Komponenten, die durch einen Punkt getrennt sind (z. B. msdn.microsoft.com). Jede Komponente kann bis zu 63 Bytes umfassen. Jeder Name kann insgesamt bis zu 255 Bytes umfassen. DNS-Namen werden im UTF-8-Zeichensatz oder Unicode dargestellt. Bei dem Namen wird die Groß- und Kleinschreibung nicht berücksichtigt. Weitere Informationen finden Sie unter [**DnsValidateName**](/windows/desktop/api/windns/nf-windns-dnsvalidatename).

Ein Computer wird eindeutig durch seinen vollqualifizierten DNS-Namen identifiziert, der aus seinem DNS-Hostnamen und dem Namen der DNS-Domäne besteht, der er zugewiesen ist. Um den vollqualifizierten DNS-Namen, DNS-Hostnamen oder DNS-Domänennamen eines Computers abzurufen, rufen Sie die [**GetComputerNameEx-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) auf. Um den DNS-Hostnamen oder DNS-Domänennamen eines Computers festzulegen, rufen Sie die [**SetComputerNameEx-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) auf. Namensänderungen werden erst wirksam, wenn der Benutzer den Computer neu startet.

NetBIOS-Namen bestehen aus bis zu 15 Bytes OEM-Zeichen, einschließlich Buchstaben, Ziffern, Bindestrichen und Zeiträumen. Einige Zeichen sind spezifisch für den Zeichensatz. NetBIOS-Namen werden in der Regel im OEM-Zeichensatz dargestellt. Der OEM-Zeichensatz hängt vom Gebietsschema ab. Einige OEM-Zeichensätze stellen bestimmte Zeichen als zwei Bytes dar. NetBIOS-Namen werden gemäß der Konvention in Großbuchstaben dargestellt, wobei der Übersetzungsalgorithmus von Kleinbuchstaben in Großbuchstaben vom OEM-Zeichensatz abhängig ist.

Die Funktionen [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) und [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) können auch den NetBIOS-Namen des Computers festlegen und abrufen. Gemäß der Konvention sind der NetBIOS-Name und der DNS-Hostname voneinander abhängig. Wenn Sie den DNS-Namen ändern, wird auch der NetBIOS-Name aktualisiert. Der NetBIOS-Name ist die OEM-Darstellung des DNS-Hostnamens bis zu MAX \_ COMPUTERNAME \_ LENGTH-Zeichen. Wenn Sie einen DNS-Hostnamen mit mehr als MAX \_ COMPUTERNAME \_ LENGTH-Zeichen festlegen, wird der NetBIOS-Name auf eine abgeschnittene Version des DNS-Hostnamens festgelegt. Andernfalls wird der gesamte DNS-Hostname in den OEM-NetBIOS-Namen übersetzt. Warnung: Wenn Sie den NetBIOS-Namen so ändern, dass es sich nicht um eine abgeschnittene Zuordnung des DNS-Namens handelt, unterbrechen Sie Anwendungen, die Funktionen wie [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) verwenden, die auf dieser Konvention basieren.

 

 
