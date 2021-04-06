---
title: Verpacken, Bereitstellung und Abfrage von Windows-apps
description: Programm gesteuertes Erstellen von App-Paketen für Windows-apps und installieren, aktualisieren, Abfragen und Deinstallieren von App-Paketen.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bfd1792e0b7b18f0dee04bca6f352e055b20f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101471"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Verpacken, Bereitstellung und Abfrage von Windows-apps

Sie können Windows-Apps (einschließlich uwps und Desktop-Apps) mithilfe von msix-/AppX-App-Paketen, die auf dem OPC-Format basieren, bereitstellen, verwalten und bereitstellen. Jedes app-Paket enthält die Dateien, die die APP bilden, und eine Manifestressource, die die Software für Windows beschreibt.

## <a name="introduction"></a>Einführung

In der Regel erstellen und Signieren Entwickler App-Pakete mithilfe von Visual Studio. Weitere Informationen finden Sie unter [Packen einer UWP-App mit Visual Studio](/windows/msix/package/packaging-uwp-apps).

Der Microsoft Store erleichtert das Erstellen, übermitteln und verkaufen Ihrer Apps für Kunden auf der ganzen Welt. Weitere Informationen finden Sie unter [App-Einreichungen](/windows/uwp/publish/app-submissions).

Mit Windows PowerShell-Cmdlets können Sie branchenspezifische Windows-apps installieren und verwalten, ohne den Store zu verwenden. Weitere Informationen finden Sie unter [AppX-Modul-Cmdlets](/powershell/module/appx/index?view=win10-ps).

Mithilfe der Paket Erstellungs-, Bereitstellungs-und Abfrage-APIs können Sie diese Aufgaben Programm gesteuert ausführen:

-   Erstellen eines App-Pakets für eine Windows-App
-   Bereitstellen einer APP mit Windows-Paket
-   Auflisten der auf einem System installierten App-Pakete und erhalten von Informationen zu diesen Paketen aus dem Manifest
-   Nutzen des Inhalts eines App-Pakets

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                    | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen eines App-Pakets (C++)](how-to-create-a-package.md)                                        | Erfahren Sie, wie Sie ein App-Paket mithilfe der Paket-API erstellen.                                                                                                                           |
| [So erstellst du ein App-Paketsignaturzertifikat](how-to-create-a-package-signing-certificate.md)      | Erfahren Sie, wie Sie mit [**Makecert**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) ein Test Code Signaturzertifikat erstellen, damit Sie Ihre APP-Pakete signieren können. |
| [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md)                    | Erfahren Sie, wie Sie [**SignTool**](/windows-hardware/drivers/devtest/signtool) zum Signieren Ihrer APP-Pakete verwenden, damit Sie bereitgestellt werden können.                                                                    |
| [Problembehandlung bei App-Paket Signatur Fehlern](how-to-troubleshoot-app-package-signature-errors.md) | Ein Fehler bei der APP-Bereitstellung kann durch einen Fehler bei der Überprüfung der digitalen Signatur des App-Pakets verursacht werden. Erfahren Sie, wie Sie diese Fehler erkennen und wie Sie damit zu tun haben.          |
| [Programm gesteuertes Signieren eines App-Pakets (C++)](how-to-programmatically-sign-a-package.md)          | Erfahren Sie, wie Sie ein App-Paket mithilfe der [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion signieren.                                                                                   |
| [So entwickeln Sie eine OEM-APP, die eine benutzerdefinierte Datei verwendet](how-to-develop-oem-app-with-custom-file.md)         | Erfahren Sie, wie Sie eine App entwickeln, die eine benutzerdefinierte Datei verwendet, um Informationen vom OEM an die APP zu übergeben.                                                                                             |
| [Inhalt des App-Pakets extrahieren (C++)](how-to-extract-content-from-a-package.md)                          | Erfahren Sie, wie Sie mithilfe der Paket-API Dateien aus einem App-Paket extrahieren.                                                                                                               |
| [Abfragen von App-Paket Manifest-Informationen (C++)](how-to-query-package-identity-information.md)                   | Erfahren Sie, wie Sie mithilfe der Pack-API Informationen aus einem App-Paket Manifest erhalten.                                                                                                            |
| [Problembehandlung](troubleshooting.md)                                                                   | Enthält Informationen, die Ihnen helfen, Probleme zu beheben, die beim Packen, bereitstellen oder Abfragen eines App-Pakets auftreten.                                                                 |
| [Paket-API-Referenz](interfaces.md)                                                                | Mit der Paket-API werden App-Pakete erstellt, gelesen und geschrieben.                                                                                                                            |
| [API-Referenz](package-deployment-api.md)                                                   | Die Bereitstellungs-API installiert, aktualisiert und deinstalliert App-Pakete.                                                                                                                    |
| [API-Referenz für Abfragen](functions.md)                                                                     | Die Abfrage-API ruft Informationen zu den App-Paketen ab, die auf dem System installiert sind.                                                                                                               |
| [Tools und PowerShell-Cmdlets](appx-packaging-tools.md)                                                 | Verwenden Sie diese Tools und Cmdlets, um App-Pakete zu erstellen, zu installieren und zu verwalten.                                                                                                              |
| [SDK-Beispiele](appx-packaging-samples.md)                                                                | Laden Sie SDK-Beispiele herunter, die die Paket Erstellung, Bereitstellung und Abfrage-APIs für Windows-apps veranschaulichen.                                                                               |
| [Glossar](appx-packaging-glossary.md)                                                                  | Erfahren Sie mehr über die Begriffe im Zusammenhang mit der Paket Erstellung, Bereitstellung und Abfrage von Windows-apps.                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzepte**
</dt> <dt>

[App-Pakete und-Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**Anderer Verweis**
</dt> <dt>

[App-Paketmanifestschema](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows. applicationmodel. Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. applicationmodel. PackageID**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 