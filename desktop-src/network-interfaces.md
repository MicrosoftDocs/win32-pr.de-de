---
description: In diesem Thema werden die Konzepte der netzwerkübergreifenden Schnittstelle für Windows beschrieben, einschließlich der Möglichkeiten, wie sie im Code und ihren Eigenschaften identifiziert werden können.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Netzwerkschnittstellen
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: d74c875b579a34464190ca039e0176b8c01bef671b0ea6c24581023a49988645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825456"
---
# <a name="network-interfaces"></a>Netzwerkschnittstellen

In diesem Thema werden die Konzepte der netzwerkübergreifenden Schnittstelle für Windows beschrieben, einschließlich der Möglichkeiten, wie sie im Code und ihren Eigenschaften identifiziert werden können. 

> [!IMPORTANT]
> Dieses Thema richtet sich an eine Entwicklergruppe, sowohl für Windows Desktopnetzwerk-Apps als auch für Kernelmodus-Netzwerktreiber. Dennoch können einige der hier vorgestellten Informationen auch für Systemadministratoren nützlich sein, die Netzwerkschnittstellen über PowerShell-Cmdlets verwalten.

## <a name="overview"></a>Übersicht

Eine *Netzwerkschnittstelle* ist der Punkt, an dem zwei Teile der Netzwerkgeräte oder Protokollebenen verbunden sind. In der Regel wird dies durch eine physische Netzwerkschnittstellenkarte (Network Interface Card, NIC) für die Verbindung zwischen einem Computer und einem privaten oder öffentlichen Netzwerk dargestellt. Sie kann jedoch auch die Form einer reinen Softwarekomponente annehmen, z. B. die Loopbackschnittstelle ( `127.0.0.1` für IPv4 oder `::1` für IPv6).

Netzwerkschnittstellen werden von der Internet Engineering Task Force (IETF) in [RFC 2863](https://tools.ietf.org/html/rfc2863) definiert und sind nicht für die Definition durch Windows vorgesehen. Ausführliche Fragen zur Bedeutung von Netzwerkschnittstellenbezeichnern wie **ifIndex** finden Sie in den IETF-Definitionen. Im weiteren Verlauf dieses Themas werden Windows-spezifische Implementierungsdetails erläutert.

## <a name="network-interface-identifiers-and-properties"></a>Netzwerkschnittstellenbezeichner und -eigenschaften

Auf Windows kann eine Netzwerkschnittstelle auf unterschiedliche Weise identifiziert werden. Einige dieser Bezeichner werden verwendet, um Netzwerkschnittstellen voneinander zu unterscheiden, aber nicht alle Bezeichner sind aufgrund ihrer unterschiedlichen Eigenschaften gleichermaßen für diese Aufgabe geeignet. Im Allgemeinen werden Netzwerkschnittstellen durch eine Netzwerkadresse für externe Komponenten identifiziert. Dies kann z. B. eine Knoten-ID und eine Portnummer oder einfach eine eindeutige Knoten-ID sein. 

Im Code kann eine Netzwerkschnittstelle auf unterschiedliche Weise identifiziert werden. In der folgenden Tabelle werden die Möglichkeiten zur Identifizierung einer Netzwerkschnittstelle zusammen mit den zugehörigen Eigenschaften aufgeführt. Es wird empfohlen, die Schnittstellen-GUID (**ifGuid**) für die Programmierung zu verwenden, es sei denn, eine bestimmte API erfordert einen anderen Netzwerkschnittstellenbezeichner.

> [!NOTE]
> In der folgenden Tabelle stellen **fett formatierte** Zellen eine Eigenschaft dar, die für Netzwerkprogrammierer wünschenswert ist.

| Bezeichner | Size | Ist im System eindeutig. | Ist weltweit einzigartig | Ist vorhersagbar | Wird wiederverwendet, wenn die NIC entfernt wird. | Persistiert bei Neustarts | Endbenutzer können jederzeit änderungen | Treiber können jederzeit geändert werden. | Allgemeine Vertrautheit mit Endbenutzern | Ist immer vorhanden |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 Bytes** | **Ja** | Nein | Nein | Ja | Nein<sup>1</sup> | **Nein** | **Nein** | **Einige**<sup>2</sup> | **Ja** |
| **NetLuid** | **8 Bytes** | **Ja** | Nein | Nein | Ja | **Ja** | **Nein** | **Nein** | Nein | **Ja** |
| **ifGuid** | **16 Bytes** | **Ja** | **Normalerweise**<sup>3</sup> | Nein | **Nein** | **Ja** | **Nein** | **Nein** | Nein | **Ja** |
| **ifAlias** | 514 Bytes | **Ja für NICs**<sup>4</sup> | Nein | Manchmal<sup>5</sup> | Ja | **Ja** | Ja | **Nein** | **Ja** | **Normalerweise**<sup>4</sup> |
| **ifDescr** | 514 Bytes | Normalerweise<sup>6</sup> | Nein | Nein | Ja | **Ja** | **Nein** | Ja | **Ja** | **Normalerweise** |
| **ifPhysAddress (MAC ADDRESS)**| 0 bis 32 Bytes | In der Regel für NICs | **In der Regel für NICs** | **Ja** | **An Hardware gebunden** | **Ja** | **Nein** | **Nein** | **Ja** | **Normalerweise** <sup>7</sup> |
| **PnP-Instanz-ID** | Bis zu 400 Bytes | **Ja** | Nein | Nein | Ja | **Ja** | **Nein** | **Nein** | Nein | **In der Regel für NICs**<sup>8</sup> |
| **PnP-Speicherort (PCI-Slotnummer)** | Bis zu 400 Bytes | **Ja** | Nein | **Ja** | Ja | **Ja** | **Nein** | **Nein** | Manchmal | Manchmal<sup>8,9</sup> |

Hinweise zur vorherigen Tabelle:

1. **IfIndexes** sind bei Neustarts nicht garantiert stabil, obwohl sie häufig den gleichen Wert wie beim vorherigen Start erhalten. Daher wird nicht empfohlen, dass Treiber **ifIndex verwenden,** es sei denn, dies ist für eine API erforderlich.
2. Einige `netsh` Befehle nehmen oder als Eingabe `ifIndex` `index` an. Daher sind einige Administrator mit der **ifIndex-Eigenschaft** vertraut, wenn sie den `netsh` Befehl häufig verwenden.
3. Wenn ein Computer geklont oder als Image verwendet wird, sind einige der GUIDs möglicherweise identisch. Darüber hinaus können bestimmte spezielle Netzwerkschnittstellen wie die integrierte Teredo-Schnittstelle auf allen Computern die gleiche GUID haben.
4. NetCfg erzwingt, dass **ifAlias** eine nicht leere Zeichenfolge ist und für alle NETZWERKKARTEN eindeutig ist. Der NDIS-Schnittstellenanbieter ist dies jedoch nicht. Daher ist es möglich, spezielle Netzwerkschnittstellen mit doppelten oder leeren Namen zu finden. Dies tritt am häufigsten bei LBFO-Teams auf.
5. Nur wenn die Firmware konsistente Gerätebenennung unterstützt. Diese Funktion wird von Servern typgesteuert verwendet.
6. NetCfg weist allen Netzwerkschnittstellen eindeutige **ifDescrs** zu. Treiber können jedoch eine API aufrufen, um **ifDescr** in etwas zu ändern, einschließlich etwas, das nicht eindeutig ist. Einige Softwarepakete von Drittanbietern tun dies.
7. Nicht alle Medientypen verfügen über eine "MAC-Adresse". Einige Tunnel verfügen beispielsweise nicht über dieses Konzept und geben einfach ein Bytearray der Länge 0 (null) als Netzwerkadresse an.
8. Nur auf Netzwerkschnittstellen vorhanden, die von einem PnP-Gerät unterstützt werden. Loopbackschnittstellen, Leichte Filterschnittstellen, schnittstellen, die von einem NDIS-Schnittstellenanbieter bereitgestellt werden, und bestimmte spezielle integrierte NICs verfügen beispielsweise nicht über PnP-Geräte, die diese unterstützen.
9. Nur einige PnP-Bus unterstützen eine PnP-Standort-ID. Die integrierten PCI- und USB-Bus-Geräte tun dies nicht, während root-enumerierte Geräte dies nicht tun.

## <a name="visibility-to-developers"></a>Sichtbarkeit für Entwickler

In der obigen Tabelle sind alle Eigenschaften mit Ausnahme der Eigenschaften von Plug & Play (PnP) für Desktop-Apps im Benutzermodus und Kernelmodustreiber über einen freigegebenen Header (Netioapi.h) sichtbar. Die PnP-Eigenschaften sind über den Devpkey.h-Header sichtbar und werden sowohl von Desktop-Apps im Benutzermodus als auch von Kernelmodustreibern verwendet. Weitere Informationen finden Sie beispielsweise in [der DEVPKEY-Dokumentation.](/windows-hardware/drivers/install/devpkey-device-instanceid)

Die [IP-Hilfsprogramm-API](/windows/desktop/IpHlp/ip-helper-start-page) ist auch für Desktop-Apps im Benutzermodus und Kernelmodustreiber verfügbar.

Die UWP-API-Oberfläche macht nur die [ifGuid-Eigenschaft](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) direkt verfügbar. Es ist jedoch möglich, dass UWP-App-Entwickler die [**GetIfTable2-Funktion**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) mit P/Invoke importieren, wenn sie auf andere Netzwerkschnittstelleneigenschaften zugreifen müssen.

## <a name="related-topics"></a>Zugehörige Themen

MiB-Definitionen (Management Information Base) für Netzwerkschnittstellen finden Sie unter [RFC 2863](https://tools.ietf.org/html/rfc2863).

Informationen zu NDIS-Netzwerkschnittstellen in Netzwerktreibern finden Sie unter [NDIS-Netzwerkschnittstellen](/windows-hardware/drivers/network/ndis-network-interfaces2).

Eine Api-Referenz für Netioapi.h finden Sie unter [netioapi.h-Header](/windows/desktop/api/netioapi/).
