---
title: Verpacken, Bereitstellung und Abfragen von Windows-Apps
description: Programmgesteuertes Erstellen von App-Paketen für Windows-Apps und Installieren, Aktualisieren, Abfragen und Deinstallieren von App-Paketen.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79d235aa8d0d69c887eb67704d30137cf36a7583471f28269ac939a26b2a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814273"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Verpacken, Bereitstellung und Abfragen von Windows-Apps

Sie stellen Apps (einschließlich UWPs und Desktop-Apps) mit msix/.appx-App-Paketen basierend auf dem OPC-Format Windows und verwalten diese. Jedes App-Paket enthält die Dateien, aus denen die App besteht, und eine Manifestdatei, die die Software beschreibt, die Windows.

## <a name="introduction"></a>Einführung

In der Regel erstellen und signieren Entwickler App-Pakete mit Visual Studio. Weitere Informationen finden Sie unter [Packen einer UWP-App mit Visual Studio](/windows/msix/package/packaging-uwp-apps).

Die Microsoft Store erleichtert das Erstellen, Übermitteln und Verkaufen Ihrer Apps an Kunden auf der ganzen Welt. Weitere Informationen finden Sie unter [App-Übermittlungen.](/windows/uwp/publish/app-submissions)

Windows PowerShell-Cmdlets ermöglichen Ihnen das Installieren und Verwalten von line-of-business-Windows-Apps, ohne die Store. Weitere Informationen finden Sie unter [Appx-Modul-Cmdlets.](/powershell/module/appx/index?view=win10-ps)

Mithilfe der ApIs für Paketierung, Bereitstellung und Abfrage können Sie diese Aufgaben programmgesteuert ausführen:

-   Erstellen eines App-Pakets für eine Windows App
-   Bereitstellen einer gepackten Windows-App
-   Aufzählen der auf einem System installierten App-Pakete und Erhalten von Informationen über diese aus dem Manifest
-   Nutzen des Inhalts eines App-Pakets

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                    | Beschreibung                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen eines App-Pakets (C++)](how-to-create-a-package.md)                                        | Erfahren Sie, wie Sie mithilfe der Paket-API ein App-Paket erstellen.                                                                                                                           |
| [So erstellst du ein App-Paketsignaturzertifikat](how-to-create-a-package-signing-certificate.md)      | Erfahren Sie, wie [**Sie makeCert**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) verwenden, um ein Testcodesignaturzertifikat zu erstellen, damit Sie Ihre App-Pakete signieren können. |
| [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md)                    | Erfahren Sie, wie [**Sie SignTool verwenden,**](/windows-hardware/drivers/devtest/signtool) um Ihre App-Pakete zu signieren, damit sie bereitgestellt werden können.                                                                    |
| [Beheben von Fehlern bei der App-Paketsignatur](how-to-troubleshoot-app-package-signature-errors.md) | Ein Fehler bei der App-Bereitstellung kann durch einen Fehler beim Überprüfen der digitalen Signatur des App-Pakets verursacht werden. Erfahren Sie, wie Sie diese Fehler erkennen und wie Sie diese probleme erkennen.          |
| [Programmgesteuertes Signieren eines App-Pakets (C++)](how-to-programmatically-sign-a-package.md)          | Erfahren Sie, wie Sie ein App-Paket mit der [**SignerSignEx2-Funktion**](/windows/desktop/SecCrypto/signersignex2) signieren.                                                                                   |
| [Entwickeln einer OEM-App, die eine benutzerdefinierte Datei verwendet](how-to-develop-oem-app-with-custom-file.md)         | Erfahren Sie, wie Sie eine App entwickeln, die eine benutzerdefinierte Datei verwendet, um Informationen vom OEM an die App zu übergeben.                                                                                             |
| [Extrahieren von App-Paketinhalten (C++)](how-to-extract-content-from-a-package.md)                          | Erfahren Sie, wie Sie Mithilfe der Paket-API Dateien aus einem App-Paket extrahieren.                                                                                                               |
| [Abfragen von App-Paketmanifestinformationen (C++)](how-to-query-package-identity-information.md)                   | Erfahren Sie, wie Sie mithilfe der Paket-API Informationen aus einem App-Paketmanifest abrufen.                                                                                                            |
| [Problembehandlung](troubleshooting.md)                                                                   | Enthält Informationen zur Behandlung von Problemen beim Packen, Bereitstellen oder Abfragen eines App-Pakets.                                                                 |
| [Referenz zur Paket-API](interfaces.md)                                                                | Die Paket-API erstellt, liest und schreibt App-Pakete.                                                                                                                            |
| [Referenz zur Bereitstellungs-API](package-deployment-api.md)                                                   | Die Bereitstellungs-API installiert, aktualisiert und deinstalliert App-Pakete.                                                                                                                    |
| [Abfrage-API-Referenz](functions.md)                                                                     | Die Abfrage-API ruft Informationen zu den app-Paketen ab, die auf dem System installiert sind.                                                                                                               |
| [Tools und PowerShell-Cmdlets](appx-packaging-tools.md)                                                 | Verwenden Sie diese Tools und Cmdlets, um App-Pakete zu erstellen, zu installieren und zu verwalten.                                                                                                              |
| [SDK-Beispiele](appx-packaging-samples.md)                                                                | Laden Sie SDK-Beispiele herunter, die die Paketierungs-, Bereitstellungs- und Abfrage-APIs für Windows veranschaulichen.                                                                               |
| [Glossar](appx-packaging-glossary.md)                                                                  | Erfahren Sie mehr über die Begriffe im Zusammenhang mit der Paketierung, Bereitstellung und Abfrage Windows Apps.                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzepte**
</dt> <dt>

[App-Pakete und Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**Weitere Referenz**
</dt> <dt>

[App-Paketmanifestschema](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows. ApplicationModel.Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel.PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 