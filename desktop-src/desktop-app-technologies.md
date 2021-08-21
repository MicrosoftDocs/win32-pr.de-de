---
description: Dieser Artikel enthält einen Index der Dokumentation zu den verfügbaren Win32-APIs für Windows Features und Technologien.
ms.assetid: FF115416-220F-4FCD-8690-F9C0890CD6CC
title: Desktop-App-Technologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd764c23b38e7239cea1d4d26d018ecbf9711b22
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812218"
---
# <a name="desktop-app-technologies"></a>Desktop-App-Technologien

Dieser Abschnitt enthält ausführliche Anleitungen und Codebeispiele zu Windows Features, die desktopanwendungen mithilfe der Win32-API zur Verfügung stehen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung  |  
|----------------------------------|---|
| [Bedienungshilfen](accessibility/accessibility.md) | Bietet Anleitungen für Entwickler Windows die barrierefreie Anwendungen entwerfen, Hilfstechnologieentwickler, die Tools wie Sprach- und Bildschirmlupe erstellen, und Softwaretesttechniker, die automatisierte Skripts zum Testen Windows erstellen. |
| [Desktop-Benutzeroberfläche](windows-application-ui-development.md) | Stellt Informationen bereit, mit denen Sie grafische Benutzeroberflächen für Ihre Apps entwickeln können, einschließlich Features wie Fenster und Nachrichten, Ressourcen und Steuerelemente. |
| [Desktopumgebung](user-interface.md) | Enthält Anleitungen zum Integrieren und Erweitern der desktopbenutzerorientierten Features von Windows, einschließlich Taskleiste, Desktop und Datei-Explorer. |
| [Anwendungsinstallation und -wartung](application-installing-and-servicing.md) | Enthält Informationen zur Verwendung von APIs und Diensten, die von Windows zum Installieren, Verwalten und Verwalten Ihrer Desktop-Apps bereitgestellt werden. |
| [Audio und Video](audio-and-video.md) | Enthält Anleitungen zur Verwendung von Audio- und Videofeatures, die von Windows. |
| [Datenzugriff und -speicherung](data-access-and-storage.md) | Enthält Informationen zu Datenzugriffs- und Speicherfeatures, die Sie in Ihren Desktopanwendungen verwenden können, einschließlich Dateisystemverwaltung und Cloudsynchronisierungs-Engines.  |
| [Geräte](devices.md) | Beschreibt APIs für die Interaktion mit Geräten und Sensoren. |
| [Diagnose](diagnostics.md) | Enthält Anleitungen zum Debuggen und zur Fehlerbehandlung, Leistungsprofilerstellung, Netzwerküberwachung und anderen Diagnosefunktionen. |
| [Dokumente und Drucken](printdocs/documents-and-printing.md) | Beschreibt die Dokumente und Druckfeatures von Windows, mit denen Anwendungen speichern, anzeigen und drucken können.  |
| [Grafik und Spiele](graphics-and-multimedia.md) | Enthält Informationen zu Grafik- und Gamingfunktionen von Windows, einschließlich DirectX und digitaler Bildverarbeitung.  |
| [Netzwerke und Internet](networking.md) | Enthält Anleitungen zu netzwerk- und internetbezogenen Features von Windows, einschließlich Netzwerkverwaltung, HTTP-APIs und Remoteprozeduraufruf (RPC). |
| [Sicherheit und Identität](security.md) | Enthält Informationen zur Authentifizierung, Autorisierung, Kryptografie und anderen Sicherheitsfeatures Windows. |
| [Systemdienste](system-services.md) | Enthält Anleitungen zu grundlegenden Betriebssystemfeatures wie Prozess und Threads, Diensten, Dynamic Link Libraries, COM, der Registrierung und mehr. |
| [KI und Machine Learning](/windows/ai/) | Nutzen Sie die Leistungsfähigkeit der Künstlichen Intelligenz, um Ihre Windows-Anwendung zu transformieren. Mit Windows KI können Sie und Ihr Unternehmen mehr erreichen, indem Sie für komplexe Probleme intelligente Lösungen bereitstellen. |

<!--
<br/>

| User Interface and accessibility | System services and fundamentals  |  Audio, video, and graphics  |
|----------------------------------|---|----|
| [Desktop User Interface](windows-application-ui-development.md)<br/>[Windows and messages](winmsg/windowing.md)<br/>[Desktop Window Manager](dwm/dwm-overview.md)<br/>[Menus and other resources](menurc/resources.md)<br/>[Dialog boxes](dlgbox/dialog-boxes.md)<br/>[Data exchange](dataxchg/data-exchange.md)<br/>[High DPI](hidpi/high-dpi-desktop-application-development-on-windows.md)<br/>[Windows controls (Win32)](controls/window-controls.md)<br/>[Desktop environment and shell](user-interface.md)<br/>[Windows Property System](properties/windows-properties-system.md)<br/>[Accessibility](accessibility.md) | [System services](system-services.md)<br/>[Component Object Model (COM)](com/component-object-model--com--portal.md)<br/>[COM+](cossdk/component-services-portal.md)<br/>[Structured storage](stg/structured-storage-start-page.md)<br/>[Dynamic-link libraries](dlls/dynamic-link-libraries.md)<br/>[Interprocess communications](ipc/interprocess-communications.md)<br/>[Memory management](memory/memory-management.md)<br/>[Power management](power/power-management-portal.md)<br/>[Processes and threads](procthread/processes-and-threads.md)<br/>[Services](services/services.md)<br/>[Synchronization](sync/synchronization.md)<br/>[Windows system information](sysinfo/windows-system-information.md) | [Audio and video technologies](audio-and-video.md)<br/>[Core Audio APIs](coreaudio/core-audio-apis-in-windows-vista.md)<br/>[DirectShow](directshow/directshow.md)<br/>[Windows Multimedia](multimedia/windows-multimedia-start-page.md)<br/>[Graphics and gaming technologies](graphics-and-multimedia.md)<br/>[DirectX](directx.md)<br/>[Direct2D](direct2d/direct2d-portal.md)<br/>[Direct3D](direct3d.md)<br/>[Windows GDI](gdi/windows-gdi.md)<br/>[GDI+](gdiplus/-gdiplus-gdi-start.md)<br/>[OpenGL](opengl/opengl.md)<br/>[Windows Imaging Component](wic/-wic-lh.md) |

<br/>

| Networking and Internet | Data access and storage  |  Devices, documents, and printing  |
|----------------------------------|---|----|
| [Networking and Internet overview](networking.md)<br/>[Remote Procedure Call](rpc/rpc-start-page.md)<br/>[Delivery optimization](delivery_optimization/delivery-optimization-portal.md)<br/>[Network interfaces](network-interfaces.md)<br/>[Network management](netmgmt/network-management.md)<br/>[Network share management](netshare/network-share-management.md)<br/>[Windows networking](wnet/windows-networking-wnet-.md)<br/>[Windows Sockets 2](winsock/windows-sockets-start-page-2.md)<br/>[Wireless networking](wireless-networking.md) | [Data access and storage overview](data-access-and-storage.md)<br/>[Local file systems](fileio/file-systems.md)<br/>[Distributed File System](dfs/distributed-file-system.md)<br/>[Projected File System](projfs/projected-file-system.md)<br/>[Cloud sync engines](cfapi/cloud-files-api-portal.md)<br/>[Virtual Storage](VStor/virtual-storage.md)<br/>[Background Intelligent Transfer Service](bits/background-intelligent-transfer-service-portal.md)<br/>[Backup](backup.md) | [Devices overview](devices.md)<br/>[Communications resources](devio/communications-resources.md)<br/>[Location API](locationapi/windows-location-api-portal.md)<br/>[Sensor API](sensorsapi/portal.md)<br/>[UPnP APIs](upnp/universal-plug-and-play-start-page.md)<br/>[Windows Portable Devices](windows-portable-devices.md)<br/>[Documents and printing](printdocs/documents-and-printing.md) |

<br/>

| Security and identity | Diagnostics and testing  |  Packaging and installation  |
|----------------------------------|---|----|
| [Security and identity overview](security.md)<br/>[Antimalware Scan Interface](amsi/antimalware-scan-interface-portal.md)<br/>[Authentication](secauthn/authentication-portal.md)<br/>[Authorization](secauthz/authorization-portal.md)<br/>[Certificate Enrollment API](seccertenroll/certenroll-portal.md)<br/>[Cryptography (CNG)](seccng/cng-portal.md)<br/>[Rights Management](SrvNodes/rights-management.md)<br/>[Security Management](secmgmt/management-portal.md)<br/>[TPM Base Services](tbs/tpm-base-services-portal.md)<br/>[Windows Biometric Framework](secbiomet/biometric-service-api-portal.md) | [Diagnostics overview](diagnostics.md)<br/>[Debugging and error handling](debugging-and-error-handling.md)<br/>[Network Monitor](netmon2/network-monitor.md)<br/>[System Monitor](sysmon/system-monitor-portal.md)<br/>[Performance counters](perfctrs/performance-counters-portal.md)<br/>[Windows error reporting](wer/windows-error-reporting.md)<br/>[Windows events](events/windows-events.md)<br/>[TraceLogging](tracelogging/trace-logging-portal.md)<br/>[Debugging tools for Windows](//docs.microsoft.com/windows-hardware/drivers/debugger/index) | [MSIX packaging](//docs.microsoft.com/windows/msix)<br/>[Application install and servicing](application-installing-and-servicing.md)<br/>[Side-by-side assemblies](sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)<br/>[Packaging and query of UWP apps](appxpkg/appx-portal.md)<br/>[Windows Installer](msi/windows-installer-portal.md)<br/>[Desktop Application Program](appxpkg/windows-desktop-application-program.md)<br/>[Windows containers](//docs.microsoft.com/virtualization/windowscontainers/about/) |

-->

<!--
:::row:::
    :::column:::
        ![User Interface and accessibility](/media/illustrations/bcs-partner-advanced-management-add-user-1.svg?branch=master)
        ### User Interface and accessibility
        * [Desktop User Interface](windows-application-ui-development.md)
        * [Windows and messages](winmsg/windowing.md)
        * [Desktop Window Manager](dwm/dwm-overview.md)
        * [Dialog boxes](dlgbox/dialog-boxes.md)
        * [Menus and other resources](menurc/resources.md)
        * [Data exchange](dataxchg/data-exchange.md)
        * [High DPI](hidpi/high-dpi-desktop-application-development-on-windows.md)
        * [Windows controls (Win32)](controls/window-controls.md)
        * [Desktop environment and shell](user-interface.md)
        * [Windows Property System](properties/windows-properties-system.md)
        * [Accessibility](accessibility.md)
    :::column-end:::
    :::column:::
        ![System and fundamentals](/media/illustrations/biztalk-get-started-get-started.svg?branch=master)
        ### System services and fundamentals
        * [System services](system-services.md)
        * [Component Object Model (COM)](com/component-object-model--com--portal.md)
        * [COM+](cossdk/component-services-portal.md)
        * [Structured storage](stg/structured-storage-start-page.md)
        * [Dynamic-link libraries](dlls/dynamic-link-libraries.md)
        * [Interprocess communications](ipc/interprocess-communications.md)
        * [Memory management](memory/memory-management.md)
        * [Power management](power/power-management-portal.md)
        * [Processes and threads](procthread/processes-and-threads.md)
        * [Services](services/services.md)
        * [Synchronization](sync/synchronization.md)
        * [Windows system information](sysinfo/windows-system-information.md)
    :::column-end:::
    :::column:::
        ![Audio, video, and graphics](/media/illustrations/virtualization-containers-samples.svg?branch=master)
        ### Audio, video, and graphics
        * [Audio and video technologies](audio-and-video.md)
        * [Core Audio APIs](coreaudio/core-audio-apis-in-windows-vista.md)
        * [DirectShow](directshow/directshow.md)
        * [Windows Multimedia](multimedia/windows-multimedia-start-page.md)
        * [Graphics and gaming technologies](graphics-and-multimedia.md)
        * [DirectX](directx.md)
        * [Direct2D](direct2d/direct2d-portal.md)
        * [Direct3D](direct3d.md)
        * [Windows GDI](gdi/windows-gdi.md)
        * [GDI+](gdiplus/-gdiplus-gdi-start.md)
        * [OpenGL](opengl/opengl.md)
        * [Windows Imaging Component](wic/-wic-lh.md)
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Networking and Internet](/media/illustrations/teams-voice-deployment.svg?branch=master)
        ### Networking and Internet
        * [Networking and Internet overview](networking.md)
        * [Remote Procedure Call](rpc/rpc-start-page.md)
        * [Delivery Optimization](delivery_optimization/delivery-optimization-portal.md)
        * [Network interfaces](network-interfaces.md)
        * [Network Management](netmgmt/network-management.md)
        * [Network Share Management](netshare/network-share-management.md)
        * [Windows Networking](wnet/windows-networking-wnet-.md)
        * [Windows Sockets 2](winsock/windows-sockets-start-page-2.md)
        * [Wireless Networking](wireless-networking.md)
    :::column-end:::
    :::column:::
        ![Data access and storage](/media/illustrations/azure-architecture-patterns.svg?branch=master)
        ### Data access and storage
        * [Data access and storage overview](data-access-and-storage.md)
        * [Local File Systems](fileio/file-systems.md)
        * [Distributed File System](dfs/distributed-file-system.md)
        * [Projected File System](projfs/projected-file-system.md)
        * [Cloud Sync Engines](cfapi/cloud-files-api-portal.md)
        * [Virtual Storage](VStor/virtual-storage.md)
        * [Background Intelligent Transfer Service](bits/background-intelligent-transfer-service-portal.md)
        * [Backup](backup.md)
    :::column-end:::
    :::column:::
        ![Devices, documents, and printing](/media/illustrations/virtualization-hperv-server-doc-archive.svg?branch=master)
        ### Devices, documents, and printing
        * [Devices overview](devices.md)
        * [Communications Resources](devio/communications-resources.md)
        * [Location API](locationapi/windows-location-api-portal.md)
        * [Sensor API](sensorsapi/portal.md)
        * [UPnP APIs](upnp/universal-plug-and-play-start-page.md)
        * [Windows Portable Devices](windows-portable-devices.md)
        * [Documents and Printing](printdocs/documents-and-printing.md)
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Security and identity](/media/illustrations/bcs-partner-advanced-management-password-3.svg?branch=master)
        ### Security and identity
        * [Security and identity overview](security.md)
        * [Antimalware Scan Interface](amsi/antimalware-scan-interface-portal.md)
        * [Authentication](secauthn/authentication-portal.md)
        * [Authorization](secauthz/authorization-portal.md)
        * [Certificate Enrollment API](seccertenroll/certenroll-portal.md)
        * [Cryptography (CNG)](seccng/cng-portal.md)
        * [Rights Management](SrvNodes/rights-management.md)
        * [Security Management](secmgmt/management-portal.md)
        * [TPM Base Services](tbs/tpm-base-services-portal.md)
        * [Windows Biometric Framework](secbiomet/biometric-service-api-portal.md)
    :::column-end:::
    :::column:::
        ![Diagnostics and testing](/media/illustrations/team-services-dev-ops-test.svg?branch=master)
        ### Diagnostics and testing
        * [Diagnostics overview](diagnostics.md)
        * [Debugging and error handling](debugging-and-error-handling.md)
        * [Network Monitor](netmon2/network-monitor.md)
        * [System Monitor](sysmon/system-monitor-portal.md)
        * [Performance counters](perfctrs/performance-counters-portal.md)
        * [Windows error reporting](wer/windows-error-reporting.md)
        * [Windows events](events/windows-events.md)
        * [TraceLogging](tracelogging/trace-logging-portal.md)
        * [Debugging tools for Windows](//docs.microsoft.com/windows-hardware/drivers/debugger/index)
    :::column-end:::
    :::column:::
        ![Packaging and installation](/media/illustrations/biztalk-host-integration-install-configure.svg?branch=master)
        ### Packaging and installation
        * [MSIX packaging and deployment](//docs.microsoft.com/windows/msix)
        * [Application Installation and Servicing](application-installing-and-servicing.md)
        * [Isolated Applications and Side-by-side Assemblies](sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
        * [Packaging, deployment, and query of UWP apps](appxpkg/appx-portal.md)
        * [Windows Installer](msi/windows-installer-portal.md)
        * [Windows Desktop Application Program](appxpkg/windows-desktop-application-program.md)
        * [Windows containers](//docs.microsoft.com/virtualization/windowscontainers/about/)
    :::column-end:::
:::row-end:::
-->
