---
description: Die Internet Protocol Suite ist das vorherrschende Netzwerkprotokoll, das in Unternehmensnetzwerken und im Internet verwendet wird.
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Winsock-Netzwerkprotokollunterstützung in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309b476669d7e27513c3e89acfbed135d425b234ccdf28a89ad74680a8cb596c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097690"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Winsock-Netzwerkprotokollunterstützung in Windows

Die Internet Protocol Suite ist das vorherrschende Netzwerkprotokoll, das in Unternehmensnetzwerken und im Internet verwendet wird. Die Internet Protocol Suite stellt eine große Sammlung von mehrstufigen Netzwerkprotokollen dar. Die Internet Protocol Suite wird häufig als TCP/IP bezeichnet und basiert auf zwei der wichtigsten Protokolle, die in der Suite enthalten sind: das Internetprotokoll (IP) und das Transmission Control Protocol (TCP).

IPv6 und IPv4 stellen die beiden verfügbaren Versionen des Internetprotokolls dar. TCP ist einer von mehreren wichtigen Netzwerkdiensten, die häufig als IP-Protokolle bezeichnet werden und über IPv6- und IPv4-Netzwerke ausgeführt werden. Das User Datagram-Protokoll (UDP) und das Internet Control Message Protocol (ICMP) sind andere wichtige IP-Protokolle, die über IPv6- und IPv4-Netzwerke verwendet werden. Es gibt eine Reihe anderer IP-Protokolle, die über IPv6- und IPv4-Netzwerke verwendet werden können.

Windows Sockets betrachtet jede Netzwerkprotokollsammlung als eindeutige Adressfamilie. Daher gilt das IPv6-Protokoll als **AF \_ INET6-Adressfamilie** und das IPv4-Protokoll als **AF \_ INET-Adressfamilie.** Die Protokolle IPv6 und IPv4 unterstützen die Verwendung verschiedener mehrstufiger IP-Protokolle wie TCP, UDP und ICMP.

Windows Sockets wurden ursprünglich entwickelt, um unterstützung für IPv4 zu Windows hinzuzufügen. Die Windows Sockets-Programmierschnittstelle wurde jedoch von Anfang an mit der Möglichkeit entwickelt, andere Netzwerkprotokollsammlungen zu unterstützen. Im Laufe der Zeit haben Versionen von Windows und die zugehörigen Windows Sockets native Unterstützung für andere Netzwerkprotokollsammlungen (z.B. IPX/SPX und AppleTalk) enthalten. Unterstützung für andere Netzwerkprotokolle war auch für Versionen von Windows als Drittanbietersoftware von Anbietern verfügbar.

Vor dem Wachstum und der Beliebtheit des Internets wurden verschiedene andere Netzwerkprotokollsammlungen in Netzwerkumgebungen verwendet, insbesondere für lokale Intranets. Die Auswahl einer Netzwerkprotokollsuite basierte häufig auf der Größe des Netzwerks oder dem Fachwissen der IT-Netzwerkmitarbeiter. Dank der heutigen globalen Internetverbindung, die selbst die kleinsten Netzwerke mit dem Rest der Welt verbindet, ist Netzwerkkenntnisse in IPv6 und IPv4 für Netzwerkexperten von entscheidender Bedeutung. Daher sind andere zuvor wichtige Netzwerkprotokollsammlungen jetzt nur noch sehr eingeschränkt genutzt und werden nun entfernt. Die native Unterstützung für diese veralteten Netzwerkprotokollsammlungen, die häufig als Legacynetzwerkprotokolle bezeichnet werden, wurde aus den aktuellen Versionen von Microsoft Windows eingestellt. Unterstützung für einige dieser Legacyprotokolle kann als Drittanbietersoftware von Anbietern (z.B. ATM mit ATM-Netzwerkhardware) verfügbar sein.

In der folgenden Tabelle werden native Windows Unterstützung für allgemeine Netzwerkprotokollsammlungen aufgeführt. 

| Netzwerkprotokoll                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Nicht unterstützt (siehe Hinweise)<br/> |
| IPv4<br/>                  | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| NetBIOS (siehe Hinweise) <br/>  | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| IrDA (siehe Hinweise)<br/>      | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| Bluetooth (siehe Hinweise)<br/> | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>     | Unterstützt<br/>                 | Unterstützt<br/>                 | Nicht unterstützt<br/>             |
| IPX/SPX<br/>               | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| Appletalk<br/>             | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Unterstützt<br/>                 | Unterstützt<br/>                 | Unterstützt<br/>                 |
| Dlc<br/>                   | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt (siehe Hinweise)<br/> | Nicht unterstützt (siehe Hinweise)<br/> | Unterstützt<br/>                 |
| ATM<br/>                   | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Unterstützt (siehe Hinweise)<br/>     | Unterstützt (siehe Hinweise)<br/>     | Unterstützt (siehe Hinweise)<br/>     |
| Netbeui<br/>               | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/> | Nicht unterstützt<br/>             | Nicht unterstützt<br/>             | Unterstützt (siehe Hinweise)<br/>     |



 

**IPv6 auf Windows 2000:** Das IPv6-Protokoll wird auf Windows 2000 mit Service Pack 1 (SP1) und höher mit Microsoft IPv6 Technology Preview für Windows 2000 unterstützt.

**NetBIOS:** Das NetBIOS-Protokoll wird häufig von Benennungsdiensten auf Windows verwendet. NetBIOS kann mehrere Netzwerkprotokollsammlungen verwenden, einschließlich IP (NetBIOS über TCP/IP), IPX/SPX und NetBEUI. Winsock unterstützt NetBIOS über TCP/IP (häufig NetBT genannt) nur für die 32-Bit-Versionen von Windows 7, Windows Server 2008 und Windows Vista. Winsock unterstützt NetBIOS über TCP/IP und NetBIOS unter Verwendung von IPX auf Windows Server 2003 und Windows XP. Winsock unterstützt NetBIOS über TCP/IP, NetBIOS mit IPX und NetBIOS unter Verwendung von NetBEUI auf Windows 2000.

**IrDA:** Das irda-Protokoll (Infrared Data Association) wird unterstützt, wenn auf dem Computer ein Port und treiber installiert sind.

**Bluetooth:** Die Winsock-Unterstützung für Bluetooth als Netzwerkprotokollsuite umfasst die Profile Bluetooth Personal Area Network (PAN) und Dial up Networking (DUN). Bluetooth Unterstützung in Windows umfasst auch die Verwendung des Bluetooth Eingabegeräte (HID) und anderer Profile zum Herstellen einer Verbindung mit Tastaturen, verweisenden Geräten und anderen Eingabegeräten, die nicht mit Netzwerkprotokollen in Zusammenhang stehen.

**DLC auf Windows 2003 und Windows XP:** Das DLC-Protokoll (Data Link Control) wird auf Windows Server 2003 und Windows XP unterstützt, wenn der in Microsoft Host Integration Server 2006, Host Integration Server 2004 oder Host Integration Server 2000 enthaltene DLC-Treiber installiert ist.

**AtM am Windows 2003, Windows XP und Windows 2000:** Das ATM-Protokoll (Asynchronous Transfer Mode) wird auf Windows Server 2003, Windows XP und Windows 2000 unterstützt, wenn ein ATM-Netzwerkadapter installiert wird. Das Protokoll für klassische IP-Adressen über ATM (manchmal als CLIP/ATM abgekürzt) wird in [RFC 2225](https://tools.ietf.org/html/rfc2225) und verwandten Dokumenten definiert, die von der IETF veröffentlicht werden. Windows Server 2003, Windows XP und Windows 2000 bieten eine vollständige Implementierung dieses Standards.

**NetBEUI auf Windows 2000:** Das NetBEUI-Protokoll wird von Windows Sockets nicht direkt unterstützt. Das NetBIOS-Protokoll, das möglicherweise mehrere Netzwerkprotokolle verwendet, unterstützt jedoch die Verwendung des NetBEUI-Protokolls auf Windows 2000.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Technische Referenz zu ATM](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[IPv6 Technology Preview für Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Irda](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[NDIS 5.0- und ATM-Unterstützung in Windows](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
