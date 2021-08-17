---
description: Transportdienstanbieter und Windows Sockets (Winsock).
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: Transportdienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d860db59b5a27d19cdc5263069161f105d79e15cfd7353789f8fdcf9944799ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927175"
---
# <a name="transport-service-providers"></a>Transportdienstanbieter

Ein angegebener Transportdienstanbieter unterstützt mindestens ein Protokoll. Beispielsweise würde ein TCP/IP-Anbieter mindestens die TCP- und UDP-Protokolle liefern, während ein IPX/SPX-Anbieter IPX, SPX und SPX II zur Verfügung stellt. Jedes Protokoll, das von einem bestimmten Anbieter unterstützt wird, wird durch eine [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) beschrieben, und der Gesamtsatz solcher Strukturen kann als Katalog der installierten Protokolle bezeichnet werden. Anwendungen können den Inhalt dieses Katalogs abrufen (weitere Informationen finden Sie unter [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)und [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)), und durch Untersuchen der verfügbaren **WSAPROTOCOL \_ INFO-Strukturen** können sie die den einzelnen Protokollen zugeordneten Kommunikationsattribute erkennen.

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>Mehrschichtige Protokolle und Protokollketten im SPI

Windows Sockets 2 unterstützt das Konzept eines mehrschichtigen Protokolls. Ein mehrschichtiges Protokoll ist ein Protokoll, das nur Kommunikationsfunktionen auf höherer Ebene implementiert, während für den eigentlichen Datenaustausch mit einem Remoteendpunkt ein zugrunde liegender Transportstapel verwendet wird. Ein Beispiel für ein solches mehrschichtige Protokoll wäre eine Sicherheitsschicht, die dem Verbindungseinrichtungsprozess Protokoll hinzufügt, um die Authentifizierung durchzuführen und ein gegenseitig vereinbartes Verschlüsselungsschema zu erstellen. Ein solches Sicherheitsprotokoll erfordert im Allgemeinen die Dienste eines zugrunde liegenden zuverlässigen Transportprotokolls wie TCP oder SPX. Der Begriff Basisprotokoll bezieht sich auf ein Protokoll wie TCP oder SPX, das vollständig in der Lage ist, Datenkommunikation mit einem Remoteendpunkt zu führen, und der Begriff Mehrschichtprotokoll wird verwendet, um ein Protokoll zu beschreiben, das nicht allein stehen kann. Eine Protokollkette würde dann als ein oder mehrere mehrschichtige Protokolle definiert werden, die zusammengekettet und durch ein Basisprotokoll verankert sind.

Diese Zeichenfolge von mehrschichtigen Protokollen und Basisprotokollen in Ketten kann erreicht werden, indem die mehrschichtigen Protokolle so anordnen, dass sie den Winsock SPI sowohl an ihren oberen als auch unteren Rändern unterstützen. Es wird [**eine spezielle WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) erstellt, die auf die Protokollkette als Ganzes verweist und die explizite Reihenfolge beschreibt, in der die mehrschichtigen Protokolle verbunden sind. Dies wird in der folgenden Grafik veranschaulicht.

![Protokollkette](images/ovrvw2-3.png)

 

 
