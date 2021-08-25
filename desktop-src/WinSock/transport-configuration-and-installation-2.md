---
description: Damit auf ein Transportprotokoll über Windows Sockets zugegriffen werden kann, muss es ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert werden.
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: Transportkonfiguration und -installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ec75810790df0d9373e8f3ee184f2dbd51d9bb5c37d7721097febe23a8aee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733240"
---
# <a name="transport-configuration-and-installation"></a>Transportkonfiguration und -installation

Damit auf ein Transportprotokoll über Windows Sockets zugegriffen werden kann, muss es ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert werden. Wenn ein Transportdienstanbieter durch Aufrufen des Installationsprogramms eines Anbieters installiert wird, müssen Konfigurationsinformationen zu einer Konfigurationsdatenbank hinzugefügt werden, um dem Ws2-32.dll informationen zum Dienstanbieter \_ zu geben. Der Ws2-32.dll exportiert mehrere \_ Installationsfunktionen, [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) und [**WSCInstallProviderAndChains,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)damit das Installationsprogramm des Anbieters die relevanten Informationen zum zu installierenden Dienstanbieter liefert. Diese Informationen umfassen beispielsweise den Namen und Pfad zur Dienstanbieter-DLL und eine Liste der [**WSAPROTOCOL \_ INFO-Strukturen,**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) die dieser Anbieter unterstützen kann. Der Ws2-32.dll stellt auch eine \_ [**Funktion, WSCDeinstallProvider,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)für das Deinstallationsprogramm eines Anbieters bereit, um alle relevanten Informationen aus der Konfigurationsdatenbank zu entfernen, die von der Ws2-Anwendung \_ verwaltet32.dll. Der genaue Speicherort und das Format dieser Konfigurationsinformationen sind für die Ws2-32.dll privat und können nur von den oben \_ genannten Funktionen bearbeitet werden.

Auf 64-Bit-Plattformen gibt es ähnliche Funktionen, die für 32-Bit- und 64-Bit-Kataloge verwendet werden. Zu diesen Funktionen [**gehören WSCInstallProvider64 \_ 32,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32) [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)und [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32).

Die Reihenfolge, in der Transportdienstanbieter zuerst installiert werden, bestimmt die Reihenfolge, in der sie über [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) und [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) an der Schnittstelle des Dienstanbieters oder über [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) an der Anwendungsschnittstelle aufzählt. Noch wichtiger ist, dass diese Reihenfolge auch die Reihenfolge bestimmt, in der Protokolle und Dienstanbieter berücksichtigt werden, wenn ein Client die Erstellung eines Sockets basierend auf der Adressfamilie, dem Typ und dem Protokollbezeichner an fordert. Windows Sockets 2 enthält ein Applet namens Sporder.exe, mit dem der Katalog installierter Protokolle interaktiv neu angeordnet werden kann, nachdem protokolle bereits installiert wurden. Windows Sockets 2 enthält auch eine zusätzliche DLL, Sporder.dll, die eine prozedurale Schnittstelle zum Neuordnen von Protokollen exportiert. Diese prozedurale Schnittstelle besteht aus einer einzelnen Prozedur namens [**WSCWriteProviderOrder.**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder)

## <a name="installing-layered-protocols-and-protocol-chains"></a>Installieren von mehrschichtigen Protokollen und Protokollketten

Die [**WSAPROTOCOL \_ INFO-Struktur,**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) die mit jedem zu installierenden Protokoll bereitgestellt wird, gibt an, ob es sich bei dem Protokoll um ein Basisprotokoll, ein mehrschichtiges Protokoll oder eine Protokollkette handelt. Der Wert des *Parameters ProtocolChain.ChainLen* wird wie in der folgenden Tabelle dargestellt interpretiert.

| Wert | Bedeutung                                           |
|-------|---------------------------------------------------|
| 0     | Mehrschichtige Protokolle.                                 |
| 1     | Basisprotokoll (oder Kette mit nur einer Komponente). |
| > 1 | Protokollkette.                                   |



 

Die Installation von Protokollketten kann nur nach erfolgreicher Installation aller Komponenten (Basisprotokolle und mehrschichtige Protokolle) erfolgen. Die [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für eine Protokollkette verwendet den *ProtocolChain-Parameter,* um die Länge der Kette und die Identität der einzelnen Komponenten zu beschreiben. Die einzelnen Protokolle, aus denen eine Kette besteht, werden in der Reihenfolge im Array ProtocolChain.ChainEntries aufgelistet, und das nullte Element des Arrays entspricht dem ersten mehrschichtigen Anbieter. Protokolle werden durch ihre *CatalogEntryID-Werte* identifiziert, die von der Ws2-32.dll zur Protokollinstallationszeit zugewiesen werden. Sie finden sie in der \_ **WSAPROTOCOL \_ INFO-Struktur** für jedes Protokoll.

Die Werte für die verbleibenden Parameter in der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) der Protokollkette sollten so ausgewählt werden, dass sie die Attribute und Bezeichner widerspiegeln, die die Protokollkette als Ganzes am besten charakterisieren. Bei der Auswahl dieser Werte sollten Entwickler bedenken, dass die Kommunikation über Protokollketten nur erfolgen kann, wenn auf beiden Endpunkten kompatible Protokollketten installiert sind und Anwendungen in der Lage sein müssen, die entsprechende **WSAPROTOCOL \_ INFO-Struktur** zu erkennen.

Wenn ein Basisprotokoll installiert wird, ist es nicht erforderlich, Einträge im *Array ProtocolChain.ChainEntries* zu erstellen. Es wird implizit verstanden, dass die einzige Komponente dieser Kette bereits im *CatalogEntryID-Parameter* der gleichen [**WSAPROTOCOL \_ INFO-Struktur identifiziert**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) wurde. Beachten Sie auch, dass Protokollketten möglicherweise nicht mehrere Instanzen desselben mehrschichtigen Protokolls enthalten.

 

 
