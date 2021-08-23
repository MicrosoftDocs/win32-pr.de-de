---
title: Informationen zur Netzwerklisten-Manager-API
description: Informationen zur Netzwerklisten-Manager-API
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704bedb3a1029c2be3c123c65a896b1765f191b886af9b354d747abd5e1698e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065173"
---
# <a name="about-the-network-list-manager-api"></a>Informationen zur Netzwerklisten-Manager-API

Die Microsoft Windows-Netzwerkumgebung ermöglicht mehrfach vernetzten Computern die gleichzeitige Verbindung mit mehreren Netzwerken. Es sind möglicherweise mehrere Drahtlosnetzwerke zusammen mit LAN- und DFÜ-Verbindungen verfügbar. Der Netzwerklisten-Manager identifiziert verfügbare Netzwerke und gibt Netzwerkattributdaten an die Anwendung zurück.

Die Netzwerklisten-Manager-API interagiert mit dem Netzwerklisten-Manager-Dienst, um Eigenschaften jedes Netzwerks zu identifizieren und abzurufen, mit dem der PC eine Verbindung herstellt. Jedes Netzwerk wird eindeutig mit einer Netzwerksignatur identifiziert, die auf den eindeutig identifizierbaren Eigenschaften dieses Netzwerks basiert. Wenn sich eine Anwendung für Netzwerklisten-Manager-Benachrichtigungen registriert, empfängt die Anwendung Benachrichtigungen über die Verfügbarkeit neuer Netzwerkverbindungen oder Änderungen an vorhandenen Netzwerkverbindungen. Anwendungen können ihre Logik je nach Netzwerk anpassen, mit dem sie verbunden sind. mit welcher Netzwerkverbindung sie verbunden sind; oder die Netzwerkeigenschaften. Mit diesen Informationen können Anwendungen ihre Aktionen basierend auf den aktuellen Netzwerkbedingungen optimieren.

Windows Vista führt neue Schnittstellen ein, die verwendet werden können, um ausführliche Informationen zu diesen Netzwerkmerkmalen und mehr zu erhalten. Mit der [**INetworkListManager-Schnittstelle**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) ist es einfach, alle Netzwerke ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) aufzulisten, die ein Computer jemals gesehen hat, oder nur die verbundenen Netzwerke oder nur die getrennten Netzwerke. Die **INetworkListManager-Schnittstelle** erleichtert auch das Auflisten der Netzwerkschnittstellen auf einem Computer.

Die [**INetwork-Schnittstelle**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) wird verwendet, um die Eigenschaften einer Netzwerkverbindung zu bestimmen: Name, Beschreibung, ID, verwaltet/authentifiziert, verbunden/getrennt usw. Es ist möglich, dass ein einzelnes Netzwerk mit mehreren Schnittstellen verbunden ist, sodass Sie über eine **INetwork-Schnittstelle** auch die Instanzen der verwendeten **INetwork-Schnittstelle** aufzählen können.

Die [**INetwork-Schnittstelle**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) informiert Sie über die relevanten Eigenschaften einer Schnittstelle: ID, GUID, Typ (verwaltet, authentifiziert) und Status (verbunden, getrennt, V4 Lokal, V4 Internet, V6 Lokal, V6 Internet). V4 Lokal bedeutet Internetprotokoll, Version 4 (IPv4) lokaler Zugriff. V4 Internet bedeutet IPv4 mit Internetzugriff. V6 Local und V6 Internet bedeuten IPv6.

Der Stamm der Objektstruktur für Netzwerkspeicherort ist die [**INetworkListManager-Schnittstelle.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) Diese Schnittstelle wird für die **CLSID \_ NetworkListManager-Co-Klasse** implementiert. Um diese Schnittstelle verwenden zu können, muss das **CLSID \_ NetworkListManager-COM-Objekt** wie gezeigt erstellt werden:


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



 

 




