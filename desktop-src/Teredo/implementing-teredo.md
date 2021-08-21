---
title: Implementieren von Teredo
ms.assetid: f32e908e-a96d-48a2-8b79-e2e53c64cb68
description: Weitere Informationen finden Sie unter Implementieren von Teredo.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b24f4524d6c513dc0a5cd11e7f6420eb7e546fa3bce75c830759fc38faaef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681650"
---
# <a name="implementing-teredo"></a>Implementieren von Teredo

Es ist zwar nicht erforderlich, Programmieränderungen für [Teredo](about-teredo.md)vorzunehmen, es wird jedoch empfohlen, dass Entwickler kleinere Änderungen vornehmen, die zur effizientesten Verwendung der Teredo-Schnittstelle führen:

-   Anwendungen, die nur IPv6-Datenverkehr nutzen können, können Teredo nutzen. Bei der Entwicklung des Anwendungsprotokolls sollte jedoch die Verarbeitung von IPv4- und IPv6-Datenverkehr berücksichtigt werden. Die Anwendung muss in Socketoptionen an AF \_ INET6 oder AF \_ UNSPEC gebunden werden.
-   Anwendungen, die auf nicht angeforderten Datenverkehr aus dem Internet lauschen können, sind erforderlich, um die Nat-Traversaloption (Network Address Translation, Netzwerkadressenübersetzung) innerhalb Windows Firewall zu aktivieren. Dies erfolgt durch Aufrufen der [**INetFwPolicy2-API,**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) bei der die Option "Edge Traversal" auf VARIANT TRUE festgelegt \_ ist. Windows Vista stellt sicher, dass die Teredo-Adresse zur Verwendung verfügbar ist, wenn eine Anwendung dies erfordert. Daher wird die Teredo-Adresse automatisch stabilisiert, wenn die Teredo-Schnittstelle verwendet wird. Wenn eine Anwendung sicherstellen möchte, dass die Teredo-Adresse stabil ist, löst der Aufruf der [**NotifyStableUnicastIpAddressTable-API**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) Teredo aus, um in einen stabilen Zustand zu überwechseln.
-   Anwendungen können auch die [IPV6 \_ PROTECTION \_ LEVEL](/windows/desktop/WinSock/ipv6-protection-level) Winsock-Socketoption verwenden, um die Schutzebene fest zu legen, die unerwünschten eingehenden Datenverkehr durch die Firewall zulässt. Weitere Informationen finden Sie unter Empfangen von nicht angeforderten Datenverkehr über [Teredo.](receiving-unsolicited-traffic-over-teredo.md)

Die Implementierung des INTERNET PROTOCOL Helper (IP Helper) bestimmter Teredo-Funktionen dient als Beispiel dafür, wie die Teredo-Adresse überprüft und einer Anwendung zur Verfügung gestellt werden kann. Weitere Informationen finden Sie unter [Verwenden von Teredo mit dem IP-Hilfser](using-teredo-with-ip-helper.md).

 

 
