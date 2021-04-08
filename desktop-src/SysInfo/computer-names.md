---
description: DNS-Namen bestehen aus einer oder mehreren Komponenten, die durch einen bestimmten Zeitraum (z. b. msdn.Microsoft.com) getrennt sind.
ms.assetid: 7e083cb5-cf0a-4284-8b54-dac856910c44
title: Computernamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf076f42e3353aa03db951e9dec428766cf4895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869227"
---
# <a name="computer-names"></a>Computernamen

DNS-Namen bestehen aus einer oder mehreren Komponenten, die durch einen bestimmten Zeitraum (z. b. msdn.Microsoft.com) getrennt sind. Jede Komponente kann bis zu 63 Bytes groß sein. Jeder Name kann bis zu 255 Bytes betragen. DNS-Namen werden im UTF-8-Zeichensatz oder im Unicode-Format dargestellt. Bei dem Namen wird die Groß- und Kleinschreibung nicht berücksichtigt. Weitere Informationen finden Sie unter [**DnsValidateName**](/windows/desktop/api/windns/nf-windns-dnsvalidatename).

Ein Computer wird durch den voll qualifizierten DNS-Namen eindeutig identifiziert, der aus dem DNS-Hostnamen und dem Namen der DNS-Domäne besteht, der er zugewiesen wurde. Rufen Sie die Funktion [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) auf, um den voll qualifizierten DNS-Namen, den DNS-Hostnamen oder den DNS-Domänen Namen eines Computers abzurufen. Um den DNS-Hostnamen und den DNS-Domänen Namen eines Computers festzulegen, müssen Sie die Funktion [**setcomputernameex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) aufrufen. Namensänderungen werden erst wirksam, wenn der Benutzer den Computer neu startet.

NetBIOS-Namen bestehen aus bis zu 15 Bytes von OEM-Zeichen, einschließlich Buchstaben, Ziffern, Bindestrichen und Punkten. Einige Zeichen sind spezifisch für den Zeichensatz. NetBIOS-Namen werden in der Regel im OEM-Zeichensatz dargestellt. Der OEM-Zeichensatz hängt vom Gebiets Schema ab. Einige OEM-Zeichensätze stellen bestimmte Zeichen als zwei Bytes dar. NetBIOS-Namen werden in Großbuchstaben dargestellt, wobei der Übersetzungs Algorithmus von Kleinbuchstaben in Großbuchstaben von OEM-Zeichensatz abhängig ist.

Die Funktionen " [**setcomputernameex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa) " und " [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) " können auch den NetBIOS-Namen des Computers festlegen und abrufen. Gemäß der Konvention sind der NetBIOS-Name und der DNS-Hostname voneinander abhängig. Wenn Sie den DNS-Namen ändern, wird der NetBIOS-Name ebenfalls aktualisiert. Der NetBIOS-Name ist die OEM-Darstellung des DNS-Host namens bis zu Max \_ . Computername- \_ Längen Zeichen. Wenn Sie einen DNS-Hostnamen mit mehr als Max \_ . Computername- \_ Längen Zeichen festlegen, wird der NetBIOS-Name auf eine gekürzte Version des DNS-Host namensfest gelegt. Andernfalls wird der gesamte DNS-Hostname in den OEM-NetBIOS-Namen übersetzt. Warnung: Wenn Sie den NetBIOS-Namen so ändern, dass er keine abgeschnittene Zuordnung des DNS-Namens ist, werden Anwendungen, die Funktionen wie [**dnshostnametocomputername**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea) verwenden, die auf dieser Konvention basieren, nicht mehr unterbrechen.

 

 
