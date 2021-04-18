---
description: Veranschaulicht die Verwendung von drahtlos gehosteten Netzwerkfunktionen.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Beispiel für drahtlos gehostete Netzwerke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368113"
---
# <a name="wireless-hosted-network-sample"></a>Beispiel für drahtlos gehostete Netzwerke

Ein Beispiel für ein drahtlos gehostetes Netzwerk, das die Verwendung von drahtlosen gehosteten Netzwerkfunktionen veranschaulicht, ist im Microsoft Windows Software Development Kit (SDK) enthalten. Die neueste Version der Windows SDK ist im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)verfügbar.

Standardmäßig ist der Quell Code des drahtlos gehosteten Netzwerks im folgenden Verzeichnis installiert:

**C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Beispiele \\ netds \\ WLAN**

Das Beispiel für drahtlos gehostete Netzwerke befindet sich im folgenden Ordner:

**Wirelesshostednetwork**

Das Beispiel für drahtlos gehostete Netzwerke kann auf der Windows SDK für Windows 7 kompiliert werden. Das Beispiel für drahtlos gehostete Netzwerke kann unter Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst ausgeführt werden.

Unter Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst wird vom Betriebssystem ein virtuelles Gerät installiert, wenn ein gehosteter netzwerkfähiger drahtloser Adapter auf dem Computer vorhanden ist. Dieses virtuelle Gerät wird normalerweise im Ordner "Netzwerkverbindungen" als "drahtlose Netzwerkverbindung 2" mit dem Gerätenamen "Microsoft Virtual WiFi Miniport Adapter" angezeigt, wenn der Computer über einen einzelnen drahtlosen Netzwerkadapter verfügt. Dieses virtuelle Gerät wird ausschließlich zum Durchführen von Verbindungen mit Software Zugriffs Punkten (softap) verwendet. Die Lebensdauer dieses virtuellen Geräts ist an den physischen drahtlosen Adapter gebunden. Wenn der physische drahtlose Adapter deaktiviert ist, wird dieses virtuelle Gerät ebenfalls entfernt.

Die drahtlosen gehosteten Netzwerkfunktionen werden verwendet, um das drahtlos gehostete Netzwerk zu starten und zu unterbinden, Einstellungen zu konfigurieren oder zu ändern oder um Informationen abzufragen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum drahtlos gehosteten Netzwerk](about-the-wireless-hosted-network.md)
</dt> <dt>

[Verwenden der Freigabe von gehosteten Netzwerken und Internet Verbindungen](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[**Wlanhustednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**Wlanhustednetworkinitsettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**Wlanhustednetworkqueryproperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**Wlanhustednetworkquerysecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**Wlanhustednetworkquerystatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**Wlanhustednetworkrefreshsecuritysettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**Wlanhustednetworksetproperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**Wlanhustednetworksetsecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**Wlanhustednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**Wlanhustednetworkstopusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**Wlanregistervirtualstationnotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



