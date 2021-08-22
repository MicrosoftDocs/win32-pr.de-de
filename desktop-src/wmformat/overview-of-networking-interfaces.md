---
title: Übersicht über Netzwerkschnittstellen
description: Übersicht über Netzwerkschnittstellen
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Medienformat-SDK, Netzwerkschnittstellen
- Windows Medienformat-SDK, Schnittstellen
- Advanced Systems Format (ASF), Netzwerkschnittstellen
- ASF (Advanced Systems Format), Netzwerkschnittstellen
- Advanced Systems Format (ASF), Schnittstellenliste für Netzwerkfeatures
- ASF (Advanced Systems Format), Schnittstellenliste für Netzwerkfeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b87da220f5ac61b7b722e79939a1fd617af46ab6608d4d92e8905f466bb98e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700262"
---
# <a name="overview-of-networking-interfaces"></a>Übersicht über Netzwerkschnittstellen

Die Netzwerkfeatures dieses SDK werden durch Methoden der folgenden Schnittstellen unterstützt.



| Schnittstelle                                                  | Beschreibung                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | Ruft Informationen zu den Clients ab, die mit einer Netzwerksenke verbunden sind.                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | Stellt eine Methode zum Erhalten von Informationen zu einem Client zur Verfügung, der an eine Writernetzwerksenke angefügt ist. Diese Schnittstelle erweitert die **IWMClientConnections-Schnittstelle.** |
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | Stellt eine Rückrufmethode zum Erfassen von Benutzeranmeldeinformationen beim Zugriff auf einen Remotestandort zur Verfügung.                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | Stellt erweiterte Methoden für das Readerobjekt zur Seite.                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | Erweitert die **IWMReaderAdvanced2-Schnittstelle.**                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | Erweitert die **IWMReaderAdvanced3-Schnittstelle.**                                                                                                         |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | Konfiguriert die Netzwerkeinstellungen für das Readerobjekt.                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | Konfiguriert zusätzliche Netzwerkeinstellungen für das Readerobjekt. Diese Schnittstelle erweitert die **IWMReaderNetworkConfig-Schnittstelle.**                         |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | Konfiguriert das Netzwerksenkenobjekt, das zum Schreiben digitaler Medien in ein Netzwerk verwendet wird.                                                                |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | Konfiguriert das Pushsenkenobjekt, das zum Verteilen digitaler Medien an Veröffentlichungspunkte verwendet wird.                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Netzwerkfunktionen**](implementing-network-functionality.md)
</dt> </dl>

 

 




