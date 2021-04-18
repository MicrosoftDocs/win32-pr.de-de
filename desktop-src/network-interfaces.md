---
description: In diesem Thema werden allgemeine Netzwerkschnittstellen Konzepte unter Windows beschrieben, einschließlich der Art und Weise, wie Sie im Code und ihren Eigenschaften identifiziert werden können.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Netzwerkschnittstellen
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: cc31be6062469750049a676807c2f8da24f473f1
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106361084"
---
# <a name="network-interfaces"></a>Netzwerkschnittstellen

In diesem Thema werden allgemeine Netzwerkschnittstellen Konzepte unter Windows beschrieben, einschließlich der Art und Weise, wie Sie im Code und ihren Eigenschaften identifiziert werden können. 

> [!IMPORTANT]
> Dieses Thema richtet sich an eine Entwicklergruppe, sowohl für Windows-Desktop Netzwerk-Apps als auch für Kernelmodustreiber. Trotzdem können einige der hier dargestellten Informationen auch für Systemadministratoren nützlich sein, die Netzwerkschnittstellen mithilfe von PowerShell-Cmdlets verwalten.

## <a name="overview"></a>Übersicht

Eine *Netzwerkschnittstelle* ist der Punkt, an dem zwei Teile der Netzwerkausrüstung oder Protokoll Ebenen eine Verbindung herstellen. Dies wird in der Regel durch eine physische Netzwerkschnittstellenkarte (NIC) für die Verbindung zwischen einem Computer und einem privaten oder öffentlichen Netzwerk repräsentiert. Es kann jedoch auch die Form einer reinen Softwarekomponente wie der Loopback Schnittstelle ( `127.0.0.1` für IPv4 oder `::1` für IPv6) annehmen.

Netzwerkschnittstellen werden von der Internet Engineering Task Force (IETF) in [RFC 2863](https://tools.ietf.org/html/rfc2863) definiert und sind nicht für die Definition durch Windows gedacht. Ausführliche Fragen zur Bedeutung von Netzwerkschnittstellen bezeichgern, wie z. b. **ifindex**, finden Sie in den IETF-Definitionen. Im weiteren Verlauf dieses Themas werden die Windows-spezifischen Implementierungsdetails erläutert.

## <a name="network-interface-identifiers-and-properties"></a>Netzwerkschnittstellen Bezeichner und-Eigenschaften

Unter Windows kann eine Netzwerkschnittstelle auf unterschiedliche Weise identifiziert werden. Einige dieser Bezeichner werden verwendet, um die Netzwerkschnittstellen voneinander zu unterscheiden, aber nicht alle Bezeichner sind aufgrund ihrer unterschiedlichen Eigenschaften gleichermaßen für diese Aufgabe geeignet. Im Allgemeinen werden Netzwerkschnittstellen durch eine Netzwerkadresse zu externen Komponenten identifiziert. Dies kann z. b. eine Knoten-ID und eine Portnummer oder einfach eine eindeutige Knoten-ID sein. 

Im Code kann eine Netzwerkschnittstelle in vielerlei Hinsicht identifiziert werden. In der folgenden Tabelle wird erläutert, wie eine Netzwerkschnittstelle zusammen mit zugeordneten Eigenschaften identifiziert werden kann. Es wird empfohlen, die Schnittstellen-GUID (**ifguid**) für die Programmierung zu verwenden, es sei denn, eine bestimmte API erfordert einen anderen Netzwerkschnittstellen Bezeichner

> [!NOTE]
> In der folgenden Tabelle stellen fett formatierten **Zellen eine Eigenschaft dar, die** für Netzwerk Programmierer wünschenswert ist.

| Bezeichner | Size | Ist im System eindeutig | Ist in der Welt eindeutig | Ist vorhersagbar | Wird wieder verwendet, wenn die NIC entfernt wurde. | Wird bei Neustarts beibehalten | Endbenutzer können jederzeit ändern. | Treiber können jederzeit geändert werden. | Allgemeine Vertrautheit mit Endbenutzern | Ist immer vorhanden |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 Bytes** | **Ja** | Nein | Nein | Ja | Nein<sup>1</sup> | **Nein** | **Nein** | **Einige**<sup>2</sup> | **Ja** |
| **Netluid** | **8 Bytes** | **Ja** | Nein | Nein | Ja | **Ja** | **Nein** | **Nein** | Nein | **Ja** |
| **ifguid** | **16 Bytes** | **Ja** | **Normalerweise**<sup>3</sup> | Nein | **Nein** | **Ja** | **Nein** | **Nein** | Nein | **Ja** |
| **ifalias** | 514 bytes | **Ja für NICs**<sup>4</sup> | Nein | Manchmal<sup>5</sup> | Ja | **Ja** | Ja | **Nein** | **Ja** | **Normalerweise**<sup>4</sup> |
| **ifdescr** | 514 bytes | Normalerweise<sup>6</sup> | Nein | Nein | Ja | **Ja** | **Nein** | Ja | **Ja** | **Gewöhnlich** |
| **ifphysaddress (Mac-Adresse)**| 0 bis 32 Bytes | Normalerweise für NICs | **Normalerweise für NICs** | **Ja** | **An Hardware gebunden** | **Ja** | **Nein** | **Nein** | **Ja** | **Normalerweise** <sup>7</sup> |
| **PNP-Instanz-ID** | Bis zu 400 bytes | **Ja** | Nein | Nein | Ja | **Ja** | **Nein** | **Nein** | Nein | **Normalerweise für NICs**<sup>8</sup> |
| **PNP-Speicherort (PCI-Slot-Nummer)** | Bis zu 400 bytes | **Ja** | Nein | **Ja** | Ja | **Ja** | **Nein** | **Nein** | Zuweilen | Manchmal<sup>8, 9</sup> |

Hinweise für die vorherige Tabelle:

1. Es ist nicht garantiert, dass **ifindexes** über Neustarts hinweg stabil sind, obwohl Sie häufig denselben Wert wie der vorherige Start erhalten. Daher empfiehlt es sich nicht, dass Treiber **ifindex** verwenden, außer wenn dies für eine API erforderlich ist.
2. Einige `netsh` Befehle übernehmen `ifIndex` oder `index` als Eingabe. Daher sind einige Administratoren mit der **ifindex** -Eigenschaft vertraut, wenn Sie den `netsh` Befehl häufig verwenden.
3. Wenn ein Computer geklont oder mit einem Image versehen wird, können einige der GUIDs identisch sein. Außerdem haben bestimmte spezielle Netzwerkschnittstellen, wie z. b. die integrierte Teredo-Schnittstelle, möglicherweise dieselbe GUID auf allen Computern.
4. Netcfg erzwingt, dass ein **ifalias** eine nicht leere Zeichenfolge ist und bei allen NICs eindeutig ist. Der NDIS-Schnittstellen Anbieter hingegen nicht. Der Grund ist, dass es möglich ist, spezielle Netzwerkschnittstellen mit doppelten oder leeren Namen zu suchen. Dies tritt am häufigsten bei LBFO-Teams auf.
5. Nur, wenn die Firmware eine konsistente Gerätebenennung unterstützt. Typcisch verfügen Server über dieses Feature.
6. Netcfg weist allen Netzwerkschnittstellen eindeutige **ifdescrs** zu. Allerdings können Treiber eine API aufgerufen werden, um die **ifdescr** in beliebige Elemente zu ändern. Dies gilt auch für etwas, das nicht eindeutig ist. Dies geschieht durch einige Softwarepakete von Drittanbietern.
7. Nicht alle Medientypen haben eine "Mac-Adresse". Beispielsweise weisen einige Tunnel nicht dieses Konzept auf und kündigen einfach ein Bytearray der Länge 0 (null) als Netzwerkadresse an.
8. Nur an Netzwerkschnittstellen vorhanden, die von einem PNP-Gerät unterstützt werden. Beispielsweise verfügen Loopback Schnittstellen, leichte Filter Schnittstellen, Schnittstellen, die von einem NDIS-Schnittstellen Anbieter bereitgestellt werden, und bestimmte spezielle integrierte NICs nicht über PNP-Geräte, die Sie unterstützen.
9. Nur einige PNP-Busse unterstützen eine PNP-Standort-ID. Die integrierten PCI-und USB-Busse funktionieren, während von Stamm aufgelisteten Geräten dies nicht der Fall ist.

## <a name="visibility-to-developers"></a>Sichtbarkeit für Entwickler

In der obigen Tabelle sind alle Eigenschaften außer den Plug & Play-Eigenschaften (PNP) für Desktop-Apps im Benutzermodus und für Kernelmodustreiber über einen freigegebenen Header ("nettioapi. h") sichtbar. Die PNP-Eigenschaften werden über den "devpkey. h"-Header angezeigt und sowohl von Desktop-Apps im Benutzermodus als auch von Kernelmodustreibern verwendet. Informationen hierzu finden Sie beispielsweise in der [devpkey](/windows-hardware/drivers/install/devpkey-device-instanceid) -Dokumentation.

Die [IP-](/windows/desktop/IpHlp/ip-helper-start-page) hilfsprogrammapi ist auch für Desktop-Apps im Benutzermodus und für Kernelmodustreiber verfügbar.

Die UWP-API-Oberfläche macht die [ifguid](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) -Eigenschaft nur direkt verfügbar. Es ist jedoch möglich, dass ein UWP-App-Entwickler die [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) -Funktion mithilfe von P/aufrufen importieren, wenn Sie auf andere Netzwerkschnittstellen Eigenschaften zugreifen müssen.

## <a name="related-topics"></a>Zugehörige Themen

Informationen zu Management Information Base (MIB)-Definitionen für Netzwerkschnittstellen finden Sie unter [RFC 2863](https://tools.ietf.org/html/rfc2863).

Informationen zu NDIS-Netzwerkschnittstellen in Netzwerk Treibern finden Sie unter [NDIS-Netzwerkschnittstellen](/windows-hardware/drivers/network/ndis-network-interfaces2).

Die API-Referenz zu "nettioapi. h" finden Sie unter " [nettioapi. h](/windows/desktop/api/netioapi/)"-Header.
