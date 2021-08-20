---
description: WMI-IP-Routenanbieter und Netzwerkklassen geben Daten für IPv4-Adressen an. Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: IPv6- und IPv4-Unterstützung in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea400d6c896220dcde5c15d40481444a77ffb309eac8bfdc50cb06ab634c384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819298"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>IPv6- und IPv4-Unterstützung in WMI

[WMI-IP-Routenanbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) und Netzwerkklassen geben Daten für IPv4-Adressen an. Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen.

## <a name="wmi-ip-data"></a>WMI-IP-Daten

Die folgenden Klassen liefern nur IPv4-Daten:

-   [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

Die folgenden Klassen geben Daten für IPv4 und IPv6 an.

-   [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    Die **IpAddess-Eigenschaft** enthält die IPv6-Adresse des Computers in einem IPv6-Netzwerk.

-   [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) kann Daten für IPv4- oder IPv6-Adressen zurückgeben.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>IPv4- und IPv6-Verbindungen mit WMI

Beim Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remotecomputer muss auf dem Zielcomputer die gleiche IP-Software wie auf dem computer ausgeführt werden, der die Verbindung herstellen soll. Beispielsweise kann ein Computer, auf dem IPv4 ausgeführt wird, keine Verbindung mit einem Computer herstellen, auf dem IPv6 ausgeführt wird, selbst wenn versucht wird, die Verbindung mithilfe eines Computernamens im Aufruf von [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md)oder mithilfe der `winmgmts` Monikerverbindung herzustellen. Das Gegenteil gilt auch: Ein Computer, auf dem nur IPv6 ausgeführt wird, kann keine Verbindung mit einem Computer herstellen, auf dem nur IPv4 ausgeführt wird.

Wenn auf dem Zielcomputer sowohl IPv4 als auch IPv6 ausgeführt werden, kann eine Verbindung von einem Computer hergestellt werden, auf dem eine der beiden IP-Software ausgeführt wird. Ein Computername oder eine IP-Adresse im IPv4- oder IPv6-Format kann in der Verbindung mit einem WMI-Namespace angegeben werden.

Ein Computer, auf dem sowohl IPv4 als auch IPv6 ausgeführt wird und der eine Verbindung mit einem Zielcomputer herstellt, auf dem nur IPv4 oder nur IPv6 ausgeführt wird, muss eine IP-Adresse im entsprechenden Format für die IP-Software des Zielcomputers angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 
