---
description: Transport Dienstanbieter und Windows Sockets (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Transport Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114eefa67bbb2d7afdf46b74f1a9524e7a77b7c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347163"
---
# <a name="transport-service-providers"></a>Transport Dienstanbieter

Ein bestimmter Transport Dienstanbieter unterstützt ein oder mehrere Protokolle. Beispielsweise würde ein TCP/IP-Anbieter mindestens die TCP-und UDP-Protokolle bereitstellen, während ein IPX/SPX-Anbieter IPX, SPX und SPX II bereitstellen kann. Jedes Protokoll, das von einem bestimmten Anbieter unterstützt wird, wird durch eine [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur beschrieben, und die Gesamtmenge dieser Strukturen kann als Katalog der installierten Protokolle betrachtet werden. Anwendungen können den Inhalt dieses Katalogs abrufen (Weitere Informationen finden Sie unter [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**wscenumprotokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)und [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)). durch Untersuchen der verfügbaren **wsaprotocol- \_ Informations** Strukturen können Sie die dem jeweiligen Protokoll zugeordneten Kommunikations Attribute ermitteln.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Geschichtete Protokolle und Protokoll Ketten in der SPI

Windows Sockets 2 bietet das Konzept eines geschichteten Protokolls. Bei einem geschichteten Protokoll handelt es sich um einen, der nur Kommunikationsfunktionen auf höherer Ebene implementiert, während er sich auf einen zugrunde liegenden Transport Stapel für den eigentlichen Datenaustausch mit einem Remote Endpunkt stützt. Ein Beispiel für ein solches mehrstufiger Protokoll wäre eine Sicherheitsebene, die dem Verbindungs Einrichtungsprozess Protokoll hinzufügt, um die Authentifizierung durchzuführen und ein einvernehmlich vereinbartes Verschlüsselungsschema einzurichten. Ein solches Sicherheitsprotokoll erfordert im Allgemeinen die Dienste eines zugrunde liegenden zuverlässigen Transport Protokolls, z. b. TCP oder SPX. Der Begriff "Basisprotokoll" bezieht sich auf ein Protokoll, wie z. b. TCP oder SPX, das vollständig die Datenkommunikation mit einem Remote Endpunkt durchführen kann. der Begriff "geschichtetes Protokoll" wird verwendet, um ein Protokoll zu beschreiben, das nicht eigenständig Eine Protokoll Kette wird dann als ein oder mehrere überlappende Protokolle definiert und durch ein Basisprotokoll verankert.

Diese überlappenden Protokolle und Basis Protokolle in Ketten können erreicht werden, indem Sie die geschichteten Protokolle anordnen, um die Winsock-SPI an Ihren oberen und unteren Rändern zu unterstützen. Es wird eine spezielle [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur erstellt, die auf die gesamte Protokoll Kette verweist und die explizite Reihenfolge beschreibt, in der die geschichteten Protokolle verknüpft werden. Dies wird in der folgenden Grafik veranschaulicht.

![Protokoll Kette](images/ovrvw2-3.png)

 

 
