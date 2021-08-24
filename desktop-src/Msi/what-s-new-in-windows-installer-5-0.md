---
description: Die Informationen in diesem Thema identifizieren die Ergänzungen und Änderungen, die in Windows Installer&\# 160;5.0 verfügbar sind.
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: Neuerungen in Windows Installer 5.0
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: 82c6ae3bf5c6781ba84d18b366998c74deedd4ca0fa4c61ac452b1d0ec409850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145223"
---
# <a name="whats-new-in-windows-installer-50"></a>Neuerungen in Windows Installer 5.0

Die Informationen in diesem Thema identifizieren die Ergänzungen und Änderungen, die in Windows Installer 5.0 verfügbar sind.

Windows Installer 5.0 ist in den folgenden Versionen von Windows enthalten:

* Client: Windows 7 und alle neueren Versionen.
* Server: Windows Server 2008 R2 und alle neueren Versionen.

> [!NOTE]
> Für Windows Installer 5.0 ist kein redistributable vorhanden. Eine Liste der für frühere Versionen von Windows Installer verfügbaren Verteilbaren finden Sie unter [Windows Installer Redistributables](windows-installer-redistributables.md). Eine vollständige Liste Windows Installer-Versionen finden Sie unter [Veröffentlichte Versionen von Windows Installer.](released-versions-of-windows-installer.md)

Diese Seite wird als Leitfaden für die Dokumentation bereitgestellt. Die tatsächlichen Betriebssystemanforderungen finden Sie im Abschnitt Anforderungen auf den Hauptverweisseiten. Teile des Windows Installers, die nicht über diese Seite mit verknüpft sind, sind möglicherweise in einer anderen Version des Windows Installers verfügbar. Informationen zu anderen Windows Installer-Versionen finden Sie unter [Neuerungen in Windows Installer.](what-s-new-in-windows-installer.md)

[Standardaktionen](standard-actions.md)

-   [MsiConfigureServices](msiconfigureservices-action.md)

[Installerfunktionen](installer-functions.md)

-   [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[Spaltendatentypen](column-data-types.md)

-   [**FormattedSDDLText**](formattedsddltext.md)

[Eigenschaften](properties.md)

-   [**MSIFASTINSTALL**](msifastinstall.md)
-   [**MSIINSTALLPERUSER**](msiinstallperuser.md)

[Zusammenfassungsinformationseigenschaften](summary-information-stream-reference.md)

-   Die [**Vorlagenzusammenfassung**](template-summary.md) enthält neue Werte, um anzugeben, dass die Datenbank mit Windows RT oder der Arm64-Plattform kompatibel ist.

[Datenbanktabellen](database-tables.md)

-   [MsiServiceConfig-Tabelle](msiserviceconfig-table.md)
-   [MsiServiceConfigFailureActions-Tabelle](msiserviceconfigfailureactions-table.md)
-   [MsiShortcutProperty-Tabelle](msishortcutproperty-table.md)
-   [MsiLockPermissionsEx-Tabelle](msilockpermissionsex-table.md)

[ControlEvents](control-events.md)

-   [MsiPrint ControlEvent](msiprint-controlevent.md)
-   [MsiLaunchApp ControlEvent](msilaunchapp-controlevent.md)

[Steuerelemente](controls.md)

-   [Linksteuerelement](hyperlink-control.md)

[Interne Konsistenzauswertungen – ICEs](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Automatisierungsschnittstelle](automation-interface.md)

-   Eigenschaften des [ **Installerobjekts**](installer-object.md)

    -   [**Installer.ClientsEx**](installer-clientsex.md)
    -   [**Installer.ComponentsEx**](installer-componentsex.md)
    -   [**Installer.ComponentPathEx**](installer-componentpathex.md)

-   Eigenschaften des [ **Components-Objekts**](components.md)

    -   [**Components.ComponentCode**](component-componentcode.md)
    -   [**Components.UserSID**](component-usersid.md)
    -   [**Components.Context**](component-context.md)

-   Eigenschaften des [ **Clientobjekts**](client.md)

    -   [**Client.ProductCode**](client-productcode.md)
    -   [**Client.ComponentCode**](client-componentcode.md)
    -   [**Client.UserSID**](client-usersid.md)
    -   [**Client.Context**](client-context.md)

-   Eigenschaften des [**ComponentInfo-Objekts**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo.Path**](componentinfo-path.md)
    -   [**ComponentInfo.State**](componentinfo-state.md)

## <a name="notes"></a>Hinweise

Setupentwickler können Windows Installer 5.0 verwenden, um ein einzelnes Installationspaket zu erstellen, das die Installation pro Computer oder pro Benutzer der Anwendung ermöglicht. Weitere Informationen finden Sie unter [Erstellen einzelner Pakete.](single-package-authoring.md) Die interne Konsistenzauswertung [ICE105](ice-105.md) überprüft, ob das Paket so erstellt wurde, dass es in einem Benutzerkontext installiert wird. Eine Anwendung, die von einem Standardbenutzer ohne Erhöhte Rechte installiert, aktualisiert, ausgeführt und entfernt werden kann, wird als Per-User-Anwendung (PUA) bezeichnet. Ein PUA kann eine bessere Benutzererfahrung bieten, Auswirkungen auf das System und andere Benutzer des Computers minimieren und UAC-Eingabeaufforderungen für Situationen reserviert, die tatsächlich die Rechteerweiterung des Benutzers erfordern. Die Single Package Authoring-Features von Windows Installer 5.0 können die Entwicklung von Per-User-Anwendungen erleichtern.

Dienstkonfigurationsoptionen ermöglichen es einem Windows Installer-Paket, die [Dienste](../services/services.md) auf einem Computer anzupassen. Weitere Informationen finden Sie unter [Using Services Configuration](using-services-configuration.md).

Ab Windows Installer 5.0 kann ein Windows Installer-Paket neue Konten, Windows [Dienste,](../services/services.md)Dateien, Ordner und Registrierungsschlüssel schützen. Die [Tabelle MsiLockPermissionsEx](msilockpermissionsex-table.md) kann einen Sicherheitsdeskriptor angeben, der Berechtigungen verweigert, die Vererbung von Berechtigungen von einer übergeordneten Ressource oder die Berechtigungen eines neuen Kontos angibt. Weitere Informationen finden Sie unter [Sichern von Ressourcen.](securing-resources-.md)

Windows Installer 5.0 kann alle auf dem Computer installierten Komponenten aufzählen und den Schlüsselpfad für die Komponente abrufen. Weitere Informationen finden Sie unter [Aufzählen von Komponenten.](enumerating-components-.md)

Windows Installer 5.0, der auf Windows Server 2012 oder Windows 8 ausgeführt wird, unterstützt die Installation genehmigter Apps auf Windows RT. Ein Windows Installer-Paket, -Patch oder -Transformation, das nicht von Microsoft signiert wurde, kann nicht auf Windows RT installiert werden. Die [**Eigenschaft Vorlagenzusammenfassung**](template-summary.md) gibt die Plattform an, die mit der Installationsdatenbank kompatibel ist und den Wert für Windows RT enthalten sollte.

Windows Installer 5.0, der auf Windows 10 auf Arm64-Prozessoren ausgeführt wird, unterstützt die Installation von Anwendungen, die speziell für die Arm64-Plattform kompiliert wurden.  Die [**Template Summary-Eigenschaft**](template-summary.md) dieser Pakete muss den Wert Arm64 enthalten. 

 
