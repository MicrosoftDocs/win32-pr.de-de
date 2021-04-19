---
description: Damit ein Transportprotokoll über Windows Sockets zugänglich ist, muss es ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert werden.
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: Transport Konfiguration und-Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea980740f727e39338c7568f4cc30a961b5484df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348771"
---
# <a name="transport-configuration-and-installation"></a>Transport Konfiguration und-Installation

Damit ein Transportprotokoll über Windows Sockets zugänglich ist, muss es ordnungsgemäß auf dem System installiert und bei Windows Sockets registriert werden. Wenn ein Transport Dienstanbieter durch Aufrufen eines Installationsprogramms eines Anbieters installiert wird, müssen Konfigurationsinformationen zu einer Konfigurations Datenbank hinzugefügt werden, damit die Ws2 \_32.dll erforderlichen Informationen zum Dienstanbieter erhalten. Der Ws2 \_ -32.dll exportiert verschiedene Installationsfunktionen, [**wscinstallprovider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) und [**wscinstallproviderandchain**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains), damit das Installationsprogramm des Herstellers die relevanten Informationen zu dem zu installierenden Dienstanbieter bereitstellt. Diese Informationen umfassen z. b. den Namen und den Pfad zur Dienstanbieter-dll und eine Liste der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Strukturen, die dieser Anbieter unterstützen kann. Der Ws2 \_ -32.dll bietet auch eine Funktion ( [**wscdeinstallprovider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)) für das Deinstallationsprogramm eines Herstellers, um alle relevanten Informationen aus der Konfigurations Datenbank zu entfernen, die von der Ws2-32.dll verwaltet wird \_ . Der genaue Speicherort und das Format dieser Konfigurationsinformationen sind für den Ws2 \_ -32.dll Privat und können nur von den oben erwähnten Funktionen bearbeitet werden.

Auf 64-Bit-Plattformen gibt es ähnliche Funktionen, die auf einem 32-Bit-und 64-Bit-Katalog ausgeführt werden. Zu diesen Funktionen gehören [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32), [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)und [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32).

Die Reihenfolge, in der Transport Dienstanbieter anfänglich installiert werden, steuert die Reihenfolge, in der Sie über [**wscenumprotokolls**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) und [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) an der Dienstanbieter Schnittstelle oder über [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) auf der Anwendungs Schnittstelle aufgelistet werden. Noch wichtiger ist, dass diese Reihenfolge auch die Reihenfolge bestimmt, in der Protokolle und Dienstanbieter berücksichtigt werden, wenn ein Client die Erstellung eines Sockets basierend auf der Adressfamilie, dem Typ und der Protokoll Kennung anfordert. Windows Sockets 2 enthält ein Applet namens Sporder.exe, mit dem der Katalog installierter Protokolle interaktiv neu angeordnet werden kann, nachdem Protokolle bereits installiert wurden. Windows Sockets 2 enthält auch eine zusätzliche dll, Sporder.dll, die eine prozedurale Schnittstelle zum Neuanordnen von Protokollen exportiert. Diese prozedurale Schnittstelle besteht aus einer einzelnen Prozedur namens [**wscschreiteproviderorder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

## <a name="installing-layered-protocols-and-protocol-chains"></a>Installieren von geschichteten Protokollen und Protokoll Ketten

Die [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur, die bei jedem zu installierenden Protokoll bereitgestellt wird, gibt an, ob das Protokoll ein Basisprotokoll, ein Überlagertes Protokoll oder eine Protokoll Kette Der Wert des *ProtocolChain. chainlen* -Parameters wird wie in der folgenden Tabelle dargestellt interpretiert.

| Wert | Bedeutung                                           |
|-------|---------------------------------------------------|
| 0     | Geschichtetes Protokoll.                                 |
| 1     | Basisprotokoll (oder Kette nur mit einer Komponente). |
| > 1 | Protokoll Kette.                                   |



 

Die Installation von Protokoll Ketten kann nur nach der erfolgreichen Installation aller Komponenten (Basis Protokolle und geschichtete Protokolle) erfolgen. Die [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für eine Protokoll Kette verwendet den *ProtocolChain* -Parameter, um die Länge der Kette und die Identität der einzelnen Komponenten zu beschreiben. Die einzelnen Protokolle, aus denen eine Kette besteht, werden in der Reihenfolge im ProtocolChain. chainentries-Array aufgelistet, wobei das nullten-Element des Arrays dem ersten geschichteten Anbieter entspricht. Protokolle werden durch ihre *catalogentryid* -Werte identifiziert, die von der Ws2 \_ -32.dll zur Protokoll Installation zugewiesen werden. Sie finden Sie in der **wsaprotocol- \_ Informations** Struktur für jedes Protokoll.

Die Werte für die restlichen Parameter in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur der Protokoll Kette sollten ausgewählt werden, um die Attribute und Bezeichner widerzuspiegeln, die die Protokoll Kette am besten als Ganzes bezeichnen. Wenn Sie diese Werte auswählen, sollten Sie Bedenken, dass die Kommunikation über Protokoll Ketten nur auftreten kann, wenn für beide Endpunkte kompatible Protokoll Ketten installiert sind und Anwendungen in der Lage sein müssen, die entsprechende **wsaprotocol- \_ Informations** Struktur zu erkennen.

Wenn ein Basisprotokoll installiert wird, ist es nicht erforderlich, Einträge im *ProtocolChain. chainentries* -Array zu erstellen. Es ist implizit zu verstehen, dass die einzige Komponente dieser Kette bereits im *catalogentryid* -Parameter der gleichen [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur identifiziert ist. Beachten Sie auch, dass Protokoll Ketten möglicherweise nicht mehrere Instanzen desselben geschichteten Protokolls enthalten.

 

 
