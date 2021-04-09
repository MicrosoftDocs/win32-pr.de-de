---
title: Informationen zur API für die Windows-Bereitstellungs Dienste
description: Bei den Windows-Bereitstellungs Diensten (Windows Deployment Services, WDS) handelt es sich um eine Suite von Komponenten, die die Bereitstellung von Windows-Betriebssystemen ermöglichen, insbesondere Windows Vista und höher und Windows Server 2008
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows-Bereitstellungs Dienste Windows-Bereitstellungs Dienste, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac4a904765f58ccf995c5bbc0a9413f8eb4d13c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948802"
---
# <a name="about-the-windows-deployment-services-api"></a>Informationen zur API für die Windows-Bereitstellungs Dienste

Bei den Windows-Bereitstellungs Diensten (Windows Deployment Services, WDS) handelt es sich um eine Suite von Komponenten, die die Bereitstellung von Windows-Betriebssystemen ermöglichen, insbesondere Windows Vista und höher und Windows Server 2008 Sie können Sie verwenden, um neue Computer mithilfe von netzwerkbasierten Installationen einzurichten.

OEMs, System Generatoren und IT-Experten von Unternehmen, die Informationen zur Bereitstellung von Windows auf neuen Computern suchen, sollten die Informationen zur standardmäßigen WDS-Lösung in den [Schritt-für-Schritt-Anleitungen für die Windows-Bereitstellungs Dienste](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) und das [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333)sehen.

In Umgebungen, in denen die standardmäßige WDS-Lösung nicht verwendet werden kann, ermöglicht die WDS-API den programmgesteuerten Zugriff auf einige WDS-Komponenten.

-   Die [Serverfunktionen der Windows-Bereitstellungs Dienste](windows-deployment-services-server-functions.md) ermöglichen den programmgesteuerten Zugriff auf den WDS-Pre-Boot Execution Environment (PXE)-Server. WDS-Serverkomponenten enthalten einen PXE-Server und Trivial File Transfer Protocol (TFTP)-Server für den Netzwerkstart eines Computers, um ein Betriebssystem zu laden und zu installieren.
-   Die [Client Funktionen der Windows-Bereitstellungs Dienste](windows-deployment-services-client-functions.md) ermöglichen den programmgesteuerten Zugriff auf den WDS-Client. Die WDS-Client Komponenten enthalten eine grafische Benutzeroberfläche, die innerhalb der Windows-Vorinstallations Umgebung (Windows PE) ausgeführt wird und mit den Serverkomponenten kommuniziert, um ein Betriebssystem Abbild auszuwählen und zu installieren.
-   Es gibt keine API für die WDS-Verwaltungs Komponenten. Bei diesen Komponenten handelt es sich um einen Satz von Tools, mit denen Sie den Server, die Betriebssystem Abbilder und die Client Computer Konten verwalten können. Weitere Informationen zu den WDS-Verwaltungs Komponenten finden Sie in [der Schritt-für-Schritt-Anleitung zur Aktualisierung der Windows-Bereitstellungs Dienste](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

Der WDS-PXE-Server besteht aus einem PXE-Server und einem PXE-Anbieter. Der PXE-Server enthält die Kern Netzwerkfunktionen. Der PXE-Server unterstützt Plug-in-Schnittstellen, die als PXE-Anbieter bezeichnet werden. Dieses Anbieter Modell ermöglicht die Entwicklung von benutzerdefinierten PXE-Lösungen, während die Kern-PXE-Server-netzwerkcodebasis weiterhin verwendet wird.

-   Entwickler können die [Server Funktionen der Windows-Bereitstellungs Dienste](windows-deployment-services-server-functions.md) verwenden, um eine DLL für einen benutzerdefinierten Anbieter zu schreiben, die in Verbindung mit der Standard-BINL (Boot Information Aushandlungs Schicht) auf einem WDS-Server ersetzt oder ausgeführt werden soll. Beispielsweise kann der benutzerdefinierte Anbieter eine Textdatei als Datenspeicher anstelle Active Directory verwenden.
-   Entwickler können die [Server Funktionen der Windows-Bereitstellungs Dienste](windows-deployment-services-server-functions.md) verwenden, um einen Filter Anbieter zu schreiben, der vor BINL oder einem anderen PXE-Anbieter in der geordneten Liste registrierter Anbieter sequenziert wird. Der zweite Anbieter bedient dann nur ausgewählte PXE-Anforderungen, während der erste Anbieter andere Anforderungen verarbeitet. So kann z. b. der zweite registrierte Anbieter in der geordneten Liste neue Funktionen bereitstellen, ohne die vorhandene im ersten Anbieter implementierte WDS-Lösung zu unterbrechen.

Der WDS-Client enthält eine grafische Benutzeroberfläche, die innerhalb der Windows-Vorinstallations Umgebung (Windows PE) ausgeführt wird und mit den Serverkomponenten kommuniziert, um ein Betriebssystem Abbild auszuwählen und zu installieren. Die WDS-Client Bibliothek unterstützt die Entwicklung von benutzerdefinierten Client Anwendungen, die einen WDS-Server verwenden können.

-   Entwickler können die [Client Funktionen der Windows-Bereitstellungs Dienste](windows-deployment-services-client-functions.md) verwenden, um eine eigene benutzerdefinierte Client Anwendung zu schreiben, die den WDS-Client ersetzt. Die benutzerdefinierte Anwendung kann z. b. die auf einem WDS-Server gespeicherten Bilder auflisten und Installations Fortschrittsmeldungen an das PXE-Server Ereignisprotokoll senden.

## <a name="windows-deployment-services-samples"></a>Beispiele für Windows-Bereitstellungs Dienste

Ein Beispiel für einen benutzerdefinierten PXE-Anbieter, Filter Anbieter und eine WDS-Client Anwendung ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Weitere Informationen finden Sie unter [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).

Sie können die folgenden WDS-Beispiele online in der [Desktop Code Gallery](https://github.com/microsoft/Windows-classic-samples)herunterladen.

<dl>

[Beispiel für Filter Anbieter für Windows-Bereitstellungs Dienste](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Bild Aufzählungs Beispiel für Windows-Bereitstellungs Dienste](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Beispiel für Multicast Consumer der Windows-Bereitstellungs Dienste](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Beispiel für Multicast Anbieter für Windows-Bereitstellungs Dienste](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Beispiel Anbieter für Windows-Bereitstellungs Dienste](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Deployment Services-Transport-Manager-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Server-API der Windows-Bereitstellungsdienste](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Verwenden der Client-API der Windows-Bereitstellungsdienste](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 