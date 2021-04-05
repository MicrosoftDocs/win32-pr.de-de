---
title: Übersicht über Netzwerkschnittstellen
description: Übersicht über Netzwerkschnittstellen
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media-Format-SDK, Netzwerkschnittstellen
- Windows Media-Format-SDK, Schnittstellen
- Advanced Systems Format (ASF), Netzwerkschnittstellen
- ASF (Advanced Systems Format), Netzwerkschnittstellen
- Advanced Systems Format (ASF), Schnittstellen Liste für Netzwerk Features
- ASF (Advanced Systems Format), Schnittstellen Liste für Netzwerk Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724131"
---
# <a name="overview-of-networking-interfaces"></a>Übersicht über Netzwerkschnittstellen

Die Netzwerk Features dieses SDK werden mithilfe von Methoden der folgenden Schnittstellen unterstützt.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmclientconnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | Ruft Informationen zu den Clients ab, die mit einer Netzwerk Senke verbunden sind.                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | Bietet eine Methode zum erhalten von Informationen zu einem Client, der an eine Writer-netzwerksenke angefügt ist Diese Schnittstelle erweitert die **iwmclientconnections** -Schnittstelle. |
| [**Iwmkredentialcallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | Stellt eine Rückruf Methode zum Abrufen von Benutzer Anmelde Informationen für den Zugriff auf eine Remote Website bereit.                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | Stellt erweiterte Methoden für das Reader-Objekt bereit.                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | Erweitert die **IWMReaderAdvanced2** -Schnittstelle.                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | Erweitert die **IWMReaderAdvanced3** -Schnittstelle.                                                                                                         |
| [**Iwmreadernetworkconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | Konfiguriert die Netzwerkeinstellungen für das Reader-Objekt.                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | Konfiguriert zusätzliche Netzwerkeinstellungen für das Reader-Objekt. Diese Schnittstelle erweitert die **iwmreadernetworkconfig** -Schnittstelle.                         |
| [**Iwmschreiternetworksink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | Konfiguriert das netzwerksink-Objekt, das zum Schreiben digitaler Medien in ein Netzwerk verwendet wird.                                                                |
| [**Iwmschreibpushsink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | Konfiguriert das Push Sink-Objekt, das zum Verteilen digitaler Medien an Publishing Points verwendet wird.                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Netzwerkfunktionen**](implementing-network-functionality.md)
</dt> </dl>

 

 




