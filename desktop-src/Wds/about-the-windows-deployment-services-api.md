---
title: Informationen zur Windows Deployment Services-API
description: Windows Deployment Services (WDS) ist eine Suite von Komponenten, die die Bereitstellung von Windows Betriebssystemen ermöglichen, insbesondere Windows Vista und höher und Windows Server 2008 und höher.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows Bereitstellungsdienste Windows Bereitstellungsdienste , Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd65f18c1628236358d61656c8c3b414d180e43166daa86dfa6562024252a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098680"
---
# <a name="about-the-windows-deployment-services-api"></a>Informationen zur Windows Deployment Services-API

Windows Deployment Services (WDS) ist eine Suite von Komponenten, die die Bereitstellung von Windows Betriebssystemen ermöglichen, insbesondere Windows Vista und höher und Windows Server 2008 und höher. Sie können damit neue Computer mithilfe von netzwerkbasierten Installationen einrichten.

OEMs, Systementwickler und IT-Experten im Unternehmen, die informationen zum Bereitstellen von Windows auf neuen Computern suchen, sollten die Informationen zur WDS-Standardlösung im [Schritt-für-Schritt-Handbuch](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) Windows Deployment Services Update und im [Windows Automated Installation Kit (OEMK)](https://www.microsoft.com/download/details.aspx?id=10333)anzeigen.

In Umgebungen, in denen die WDS-Standardlösung nicht verwendet werden kann, ermöglicht die WDS-API den programmgesteuerten Zugriff auf einige WDS-Komponenten.

-   Die [Windows Deployment Services-Serverfunktionen](windows-deployment-services-server-functions.md) bieten programmgesteuerten Zugriff auf den WDS-Pre-Boot eXecution Environment-Server (PXE). WDS-Serverkomponenten umfassen einen PXE-Server und einen TFTP-Server (Trivial File Transfer Protocol), um einen Computer zum Laden und Installieren eines Betriebssystems über das Netzwerk zu starten.
-   Die [Windows Deployment Services-Clientfunktionen](windows-deployment-services-client-functions.md) bieten programmgesteuerten Zugriff auf den WDS-Client. Die WDS-Clientkomponenten enthalten eine grafische Benutzeroberfläche, die innerhalb der Windows Pre-Installation Environment (Windows PE) ausgeführt wird und mit den Serverkomponenten kommuniziert, um ein Betriebssystemimage auszuwählen und zu installieren.
-   Es gibt keine API für die WDS-Verwaltungskomponenten. Bei diesen Komponenten handelt es sich um eine Reihe von Tools, die Sie zum Verwalten des Servers, der Betriebssystemimages und der Clientcomputerkonten verwenden. Weitere Informationen zu den WDS-Verwaltungskomponenten finden Sie unter [The Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

Der WDS-PXE-Server besteht aus einem PXE-Server und einem PXE-Anbieter. Der PXE-Server enthält die Kernnetzwerkfunktion. Der PXE-Server unterstützt Plug-In-Schnittstellen, die als PXE-Anbieter bezeichnet werden. Dieses Anbietermodell ermöglicht die Entwicklung benutzerdefinierter PXE-Lösungen, während weiterhin die Kerncodebasis für PXE-Servernetzwerke verwendet wird.

-   Entwickler können die [Windows Deployment Services-Serverfunktionen](windows-deployment-services-server-functions.md) verwenden, um eine DLL für einen benutzerdefinierten Anbieter zu schreiben, die auf einem WDS-Server in Verbindung mit der standardmäßigen Boot Information Negotiation Layer (BINL) ersetzt oder ausgeführt wird. Beispielsweise kann der benutzerdefinierte Anbieter anstelle von Active Directory eine Textdatei als Datenspeicher verwenden.
-   Entwickler können die [Windows Deployment Services-Serverfunktionen](windows-deployment-services-server-functions.md) verwenden, um einen Filteranbieter zu schreiben, der vor BINL oder einem anderen PXE-Anbieter in der sortierten Liste der registrierten Anbieter sequenziert wird. Der zweite Anbieter verarbeitet dann nur ausgewählte PXE-Anforderungen, während der erste Anbieter andere Anforderungen verarbeitet. Dies kann beispielsweise dem zweiten registrierten Anbieter in der sortierten Liste ermöglichen, neue Funktionen anzubieten, ohne die vorhandene WDS-Lösung zu unterbrechen, die im ersten Anbieter implementiert ist.

Der WDS-Client enthält eine grafische Benutzeroberfläche, die in der Windows Pre-Installation Environment (Windows PE) ausgeführt wird und mit den Serverkomponenten kommuniziert, um ein Betriebssystemimage auszuwählen und zu installieren. Die WDS-Clientbibliothek unterstützt die Entwicklung benutzerdefinierter Clientanwendungen, die einen WDS-Server verwenden können.

-   Entwickler können die [Windows Deployment Services-Clientfunktionen](windows-deployment-services-client-functions.md) verwenden, um ihre eigene benutzerdefinierte Clientanwendung zu schreiben, die den WDS-Client ersetzt. Beispielsweise kann die benutzerdefinierte Anwendung die auf einem WDS-Server gespeicherten Images aufzählen und Meldungen zum Installationsfortschritt an das PXE-Serverereignisprotokoll senden.

## <a name="windows-deployment-services-samples"></a>Windows Beispiele für Bereitstellungsdienste

Ein benutzerdefinierter PXE-Beispielanbieter, Filteranbieter und eine WDS-Clientanwendung sind im Microsoft Windows Software Development Kit (SDK) verfügbar. Weitere Informationen finden Sie unter [Microsoft Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)

Sie können die folgenden WDS-Beispiele online im [Desktopcodekatalog](https://github.com/microsoft/Windows-classic-samples)herunterladen.

<dl>

[Windows Beispiel für Bereitstellungsdienste-Filteranbieter](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Beispiel für die Imageenumeration von Bereitstellungsdiensten](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Windows Multicast-Consumerbeispiel für Bereitstellungsdienste](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Beispiel für Multicastanbieter für Bereitstellungsdienste](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Beispiel für Bereitstellungsdiensteanbieter](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Transport-Manager-Beispiel für Bereitstellungsdienste](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Server-API der Windows-Bereitstellungsdienste](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Verwenden der Client-API der Windows-Bereitstellungsdienste](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 