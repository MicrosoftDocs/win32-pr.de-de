---
description: WMI-IP-Routen Anbieter und Netzwerk Klassen stellen Daten für IPv4-Adressen bereit. Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: IPv6-und IPv4-Unterstützung in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363246"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a>IPv6-und IPv4-Unterstützung in WMI

WMI [-IP-Routen Anbieter](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) und Netzwerk Klassen stellen Daten für IPv4-Adressen bereit. Ab Windows Vista bietet WMI auch eingeschränkte Unterstützung für IPv6-Netzwerkfunktionen.

## <a name="wmi-ip-data"></a>WMI-IP-Daten

Die folgenden Klassen stellen nur IPv4-Daten bereit:

-   [**Win32- \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**Win32- \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**Win32- \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**Win32- \_ activeroute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**Win32- \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

Die folgenden Klassen stellen Daten sowohl für IPv4 als auch für IPv6 bereit.

-   [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    Die **ipaddess** -Eigenschaft enthält die IPv6-Adresse des Computers in einem IPv6-Netzwerk.

-   [**Win32 \_ Pingstatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ Pingstatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) kann Daten für IPv4-oder IPv6-Adressen zurückgeben.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>IPv4-und IPv6-Verbindungen mit WMI

Beim Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remote Computer muss auf dem Bereitstellungs Zielcomputer die gleiche IP-Software wie der Computer ausgeführt werden, der die Verbindung herstellt. Beispielsweise kann ein Computer, auf dem IPv4 ausgeführt wird, keine Verbindung mit einem Computer herstellen, auf dem IPv6 ausgeführt wird. Dies gilt auch, wenn versucht wird, einen Computernamen im Aufruf von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**Swap-Locator. ConnectServer**](swbemlocator-connectserver.md)oder mithilfe der `winmgmts` monikerverbindung zu verwenden. Das Gegenteil gilt auch: ein Computer, auf dem nur IPv6 ausgeführt wird, kann keine Verbindung mit einem Computer herstellen, der nur IPv4 ausgeführt

Wenn auf dem Bereitstellungs Zielcomputer sowohl IPv4 als auch IPv6 ausgeführt wird, kann eine Verbindung von einem Computer hergestellt werden, auf dem entweder eine IP-Software ausgeführt wird. Ein Computername oder eine IP-Adresse im IPv4-oder IPv6-Format kann in der Verbindung mit einem WMI-Namespace bereitgestellt werden.

Ein Computer, auf dem sowohl IPv4 als auch IPv6 ausgeführt wird und der eine Verbindung mit einem Zielcomputer herstellt, auf dem nur IPv4 oder IPv6 ausgeführt wird, muss eine IP-Adresse im entsprechenden Format für die IP-Software des Ziel Computers

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu WMI](about-wmi.md)
</dt> </dl>

 

 
