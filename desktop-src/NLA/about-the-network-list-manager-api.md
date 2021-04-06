---
title: Informationen zur Netzwerk Listen-Manager-API
description: Informationen zur Netzwerk Listen-Manager-API
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713589"
---
# <a name="about-the-network-list-manager-api"></a>Informationen zur Netzwerk Listen-Manager-API

Mit der Microsoft Windows-Netzwerkumgebung können mehrfach vernetzte Computer gleichzeitig eine Verbindung mit mehreren Netzwerken herstellen. Möglicherweise sind mehrere Drahtlos Netzwerke zusammen mit LAN-und DFÜ-Verbindungen verfügbar. Der Netzwerk Listen-Manager identifiziert verfügbare Netzwerke und gibt Netzwerk Attributdaten an die Anwendung zurück.

Die Netzwerk Listen-Manager-API interagiert mit dem Netzwerk Listen-Manager-Dienst, um die Eigenschaften jedes Netzwerks zu identifizieren und abzurufen, mit dem der PC eine Verbindung herstellt. Jedes Netzwerk wird durch eine Netzwerk Signatur basierend auf den eindeutig identifizierbaren Eigenschaften dieses Netzwerks eindeutig identifiziert. Wenn eine Anwendung für Benachrichtigungen des Netzwerk Listen-Managers registriert wird, erhält die Anwendung Benachrichtigungen über die Verfügbarkeit neuer Netzwerkverbindungen oder Änderungen an vorhandenen Netzwerkverbindungen. Anwendungen können Ihre Logik abhängig von dem Netzwerk anpassen, mit dem Sie verbunden sind. die Netzwerkverbindung, mit der Sie verbunden sind; oder die Netzwerk Eigenschaften. Mit diesen Informationen können Anwendungen ihre Aktionen basierend auf den aktuellen Netzwerkbedingungen optimieren.

In Windows Vista werden neue Schnittstellen eingeführt, die verwendet werden können, um ausführliche Informationen zu diesen Netzwerk Merkmalen und mehr zu erhalten. Mit der [**inetworklistmanager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) -Schnittstelle ist es ganz einfach, alle Netzwerke ([**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)), die ein Computer jemals gesehen hat, oder nur die verbundenen Netzwerke aufzuzählen. Die **inetworklistmanager** -Schnittstelle vereinfacht auch das Auflisten der Netzwerkschnittstellen auf einem Computer.

Die [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) -Schnittstelle wird verwendet, um die Eigenschaften einer Netzwerkverbindung zu bestimmen: Name, Beschreibung, ID, verwaltet/authentifiziert, verbunden/getrennt und mehr. Es ist möglich, dass ein einzelnes Netzwerk mit mehreren Schnittstellen verbunden ist, sodass Sie über eine **iNetwork** -Schnittstelle auch die Instanzen der verwendeten **iNetwork** -Schnittstelle auflisten können.

Die [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) -Schnittstelle zeigt Ihnen die relevanten Eigenschaften einer Schnittstelle an: ID, Guid, Typ (verwaltet, authentifiziert) und Status (verbunden, getrennt, v4 lokal, v4-Internet, V6 local, V6 Internet). V4 local bedeutet lokalen IPv4-Zugriff (Internet Protocol Version 4). V4 Internet bedeutet IPv4 mit Internet Zugang. V6 local und V6 Internet bedeuten IPv6.

Der Stamm der Objektstruktur für Network Location ist die [**inetworklistmanager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) -Schnittstelle. Diese Schnittstelle wird in der **CLSID \_ networklistmanager** -Co-Klasse implementiert. Um diese Schnittstelle verwenden zu können, muss das COM-Objekt " **CLSID \_ networklistmanager** " wie folgt erstellt werden:


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




