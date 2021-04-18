---
description: Die Internet Protokoll Suite ist das vorherrschende Netzwerkprotokoll, das in Unternehmensnetzwerken und über das Internet verwendet wird.
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Winsock-Netzwerkprotokoll Unterstützung in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36da53101dda06426a04e5f910b4548273e8ab47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484926"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Winsock-Netzwerkprotokoll Unterstützung in Windows

Die Internet Protokoll Suite ist das vorherrschende Netzwerkprotokoll, das in Unternehmensnetzwerken und über das Internet verwendet wird. Die Internet Protokoll Suite stellt eine große Auflistung von geschichteten Netzwerkprotokollen dar. Die Internetprotokoll Suite wird häufig als TCP/IP bezeichnet, basierend auf zwei der wichtigsten Protokolle, die in der Suite enthalten sind: das Internetprotokoll (IP) und das Transmission Control Protocol (TCP).

IPv6 und IPv4 stellen die beiden verfügbaren Versionen des Internet Protokolls dar. TCP ist einer von mehreren wichtigen Netzwerkdiensten, die häufig als IP-Protokolle bezeichnet werden, die über IPv6-und IPv4-Netzwerke betrieben werden. Das User Datagram-Protokoll (UDP) und das ICMP (Internet Control Message Protocol) sind andere wichtige IP-Protokolle, die über IPv6-und IPv4-Netzwerke verwendet werden. Es gibt eine Reihe anderer IP-Protokolle, die über IPv6-und IPv4-Netzwerke verwendet werden können.

Windows Sockets betrachtet jede Netzwerkprotokoll Suite als eindeutige Adressfamilie. Das IPv6-Protokoll wird also als " **AF \_ inet6** Address Family" betrachtet, und das IPv4-Protokoll wird als " **AF \_ inet** Address Family" betrachtet. Die IPv6-und IPv4-Protokolle unterstützen die Verwendung verschiedener über Lagertem IP-Protokolle wie TCP, UDP und ICMP.

Windows Sockets wurden anfänglich entwickelt, um Unterstützung für IPv4 zu Windows hinzuzufügen. Allerdings wurde die Windows Sockets-Programmierschnittstelle von Anfang an mit der Möglichkeit entworfen, andere Netzwerkprotokoll Suites zu unterstützen. Im Laufe der Zeit enthalten Versionen von Windows und die zugehörigen Windows-Sockets systemeigene Unterstützung für andere Netzwerkprotokoll-Suites (z. b. IPX/SPX und AppleTalk). Unterstützung für andere Netzwerkprotokolle war auch für Windows-Versionen als Drittanbieter Software von Anbietern verfügbar.

Vor dem Wachstum und der Beliebtheit des Internets wurden verschiedene andere Netzwerkprotokoll Suites in Netzwerkumgebungen verwendet, insbesondere für lokale Intranets. Die Auswahl einer Netzwerkprotokoll Suite basiert häufig auf der Netzwerkgröße oder den Fachkenntnissen des IT-Netzwerk Personals. Dank der heutigen globalen Internet Konnektivität, die sogar die kleinsten Netzwerke mit dem Rest der Welt verknüpft, ist das Netzwerk Fachwissen in IPv6 und IPv4 für Netzwerkexperten von entscheidender Bedeutung. Folglich sind andere zuvor wichtige Netzwerk-Protokoll Suites jetzt sehr eingeschränkt und werden nicht mehr verwendet. Die systemeigene Unterstützung für diese überflüssig erten Netzwerkprotokoll Suites, häufig als ältere Netzwerkprotokolle bezeichnet, wurde aus den neueren Versionen von Microsoft Windows entfernt. Unterstützung für einige dieser Legacy Protokolle kann als Drittanbieter Software von Anbietern (z. b. ATM mit ATM-Netzwerkhardware) verfügbar sein.

In der folgenden Tabelle ist die systemeigene Windows-Unterstützung für allgemeine Netzwerkprotokoll Sammlungen aufgeführt. 

| Netzwerkprotokoll                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Nicht unterstützt (siehe Hinweise)<br/> |
| IPv4<br/>                  | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| NetBIOS (siehe Hinweise) <br/>  | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| Irren (siehe Hinweise)<br/>      | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| Bluetooth (siehe Hinweise)<br/> | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Nicht unterstützt<br/>             |
| IPX/SPX<br/>               | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| AppleTalk<br/>             | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| DLC<br/>                   | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt (siehe Hinweise)<br/> | Nicht unterstützt (siehe Hinweise)<br/> | Unterstützt<br/>                 |
| ATM<br/>                   | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Unterstützt (siehe Hinweise)<br/>     | Unterstützt (siehe Hinweise)<br/>     | Unterstützt (siehe Hinweise)<br/>     |
| NetBEUI<br/>               | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/>             | Nicht unterstützt<br/>             | Unterstützt (siehe Hinweise)<br/>     |



 

**IPv6 unter Windows 2000:** Das IPv6-Protokoll wird unter Windows 2000 mit Service Pack 1 (SP1) und höher mit der Microsoft IPv6-Technologievorschau für Windows 2000 unterstützt.

**NetBIOS:** Das NetBIOS-Protokoll wird häufig durch Benennen von Diensten unter Windows verwendet. NetBIOS kann mehrere Netzwerkprotokoll Suites verwenden, einschließlich IP (NetBIOS über TCP/IP), IPX/SPX und NetBEUI. Winsock unterstützt NetBIOS über TCP/IP (häufig als NetBT bezeichnet) nur in den 32-Bit-Versionen von Windows 7, Windows Server 2008 und Windows Vista. Winsock unterstützt NetBIOS über TCP/IP und NetBIOS mithilfe von IPX unter Windows Server 2003 und Windows XP. Winsock unterstützt NetBIOS über TCP/IP, NetBIOS mithilfe von IPX und NetBIOS unter Verwendung von NetBEUI unter Windows 2000.

Nicht mehr **:** Das UNDA-Protokoll (Infrarot Data Association) wird unterstützt, wenn auf dem Computer ein Infrarot Anschluss und ein installierter Treiber installiert sind.

**Bluetooth:** Die Winsock-Unterstützung für Bluetooth als Netzwerkprotokoll Suite umfasst die Bluetooth-PCs (Personal Area Network) und Dun-profile (Dial up Network). Die Bluetooth-Unterstützung in Windows umfasst auch die Verwendung des Bluetooth-Eingabegeräte (HID) und anderer Profile für das Herstellen einer Verbindung mit Tastaturen, zeige Geräten und anderen Eingabegeräten, die nicht mit Netzwerkprotokollen verknüpft sind.

**DLC unter Windows 2003 und Windows XP:** Das Data Link Control DLC-Protokoll (DLC) wird unter Windows Server 2003 und Windows XP unterstützt, wenn der DLC-Treiber, der in Microsoft Host Integration Server 2006, Host Integration Server 2004 oder Host Integration Server 2000 enthalten ist, installiert ist.

**ATM unter Windows 2003, Windows XP und Windows 2000:** Das Protokoll des asynchronen Übertragungsmodus (ATM) wird unter Windows Server 2003, Windows XP und Windows 2000 unterstützt, wenn ein ATM-Netzwerkadapter installiert ist. Das Protokoll für die klassische IP über ATM (manchmal als "Clip/ATM" abgekürzt) ist in [RFC 2225](https://tools.ietf.org/html/rfc2225) und den zugehörigen Dokumenten definiert, die vom IETF veröffentlicht wurden. Windows Server 2003, Windows XP und Windows 2000 bieten eine vollständige Implementierung dieses Standards.

**NetBEUI unter Windows 2000:** Das NetBEUI-Protokoll wird von Windows Sockets nicht direkt unterstützt. Das NetBIOS-Protokoll, das möglicherweise mehrere Netzwerkprotokolle verwendet, unterstützt jedoch die Verwendung des NetBEUI-Protokolls unter Windows 2000.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Technische Referenz für ATM](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[IPv6-Technologievorschau für Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[IrDA](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[Unterstützung für NDIS 5,0 und ATM in Windows](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
