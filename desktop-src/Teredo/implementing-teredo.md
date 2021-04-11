---
title: Implementieren von Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: 'Weitere Informationen: Implementieren von Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffdf2859d3742bea02e240c6a26bd0e4ade85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218326"
---
# <a name="implementing-teredo"></a>Implementieren von Teredo

Es ist zwar nicht erforderlich, Programmier Änderungen für [Teredo](about-teredo.md)vorzunehmen, aber es wird empfohlen, dass Entwickler kleinere Änderungen vornehmen, die zur effizientesten Verwendung der Teredo-Schnittstelle führen:

-   Anwendungen, die nur den IPv6-Datenverkehr für die Verwendung von Teredo verwenden können, sind möglich. Bei der Entwicklung des Anwendungs Protokolls sollte jedoch die Verarbeitung von IPv4-und IPv6-Datenverkehr berücksichtigt werden. Die Anwendung muss \_ in Socketoptionen an AF inet6 oder AF \_ unspec gebunden werden.
-   Anwendungen, die den nicht angeforderten Datenverkehr aus dem Internet überwachen können, sind erforderlich, um die NAT-Durchlauf Option (Network Address Translation) in der Windows-Firewall zu aktivieren. Dies wird erreicht, indem die [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) -API aufgerufen wird, wobei die Option "Edge-Traversal" auf Variant true festgelegt ist \_ . Windows Vista stellt sicher, dass die Teredo-Adresse zur Verwendung verfügbar ist, wenn Sie von einer Anwendung benötigt wird. Folglich wird die Teredo-Adresse automatisch stabilisiert, wenn die Teredo-Schnittstelle verwendet wird. Wenn eine Anwendung sicherstellen möchte, dass die Teredo-Adresse stabil ist, löst der Aufruf der [**notifystableunicastipadresssstable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) -API Teredo aus, um in einen stabilen Zustand zu wechseln.
-   Anwendungen können auch die Option "Winsock-Socket" der [IPv6- \_ Schutz \_ Ebene](/windows/desktop/WinSock/ipv6-protection-level) verwenden, um die Schutz Ebene festzulegen, die den nicht angeforderten eingehenden Datenverkehr durch die Firewall ermöglicht. Weitere Informationen finden Sie unter [empfangen von angefordertem Datenverkehr über Teredo](receiving-unsolicited-traffic-over-teredo.md) .

Die IP-Hilfsanwendung (Internet Protocol Helper, IP-Hilfsobjekt) spezifischer Teredo-Funktionen dient als Beispiel dafür, wie die Teredo-Adresse überprüft und einer Anwendung zur Verfügung gestellt werden kann. Weitere Informationen finden Sie unter [Verwenden von Teredo mit IP-](using-teredo-with-ip-helper.md)Hilfsprogramm.

 

 
