---
description: Die auf dieser Seite aufgeführten Windows Installer-Funktionen, -Tabellen und -Eigenschaften werden von Windows Installer&\# 160;4.5 und früheren Versionen nicht unterstützt.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: Nicht unterstützt in Windows Installer 4.5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a285094610f0a00a39a26bb2d0683cb41afdfa3ed126ac27f7655c3cd56df17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979350"
---
# <a name="not-supported-in-windows-installer-45"></a>Nicht unterstützt in Windows Installer 4.5

Die auf dieser Seite aufgeführten Windows Installer-Funktionen, -Tabellen und -Eigenschaften werden von Windows Installer 4.5 und früheren Versionen nicht unterstützt. Das Fehlen eines Features in dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Hauptdokumentation erfahren Sie, welche Windows Installer-Version für ein bestimmtes Feature erforderlich ist. Informationen zu anderen Windows Installer-Versionen finden Sie unter [Neuerungen in Windows Installer.](what-s-new-in-windows-installer.md)

Windows Installer 4.5 ist als redistributable für Windows Server 2008, Windows Vista mit Service Pack 1 (SP1), Windows XP mit Service Pack 2 (SP2) und höher und Windows Server 2003 mit Service Pack 1 (SP1) und höher verfügbar. Eine vollständige Liste aller Windows Installer-Versionen und verteilbaren Versionen finden Sie unter [Veröffentlichte Versionen von Windows Installer.](released-versions-of-windows-installer.md)

Die folgenden Features werden in Windows Installer 4.5 und früheren Versionen nicht unterstützt.

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
-   [Bitmap-Steuerelementunterstützung](bitmap-control.md) von WIC-Bilddateiformaten

[Interne Konsistenzauswertungen – ICEs](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Automatisierungsschnittstelle](automation-interface.md)

-   Eigenschaften des [ **Installerobjekts**](installer-object.md)

    -   [**Installer.ClientsEx**](installer-clientsex.md)
    -   [**Installer.ComponentsEx**](installer-componentsex.md)
    -   [**Installer.ComponentPathEx**](installer-componentpathex.md)

-   Eigenschaften des [ **Komponentenobjekts**](components.md)

    -   [**Component.ComponentCode**](component-componentcode.md)
    -   [**Component.UserSID**](component-usersid.md)
    -   [**Component.Context**](component-context.md)

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

Windows Installer 4.5 unterstützt einige Features nicht, mit denen ein einzelnes Installationspaket entweder im Computer- oder benutzerbezogenen Installationskontext installiert werden kann. Weitere Informationen finden Sie unter [Erstellen einzelner Pakete.](single-package-authoring.md)

Windows Installer 4.5 unterstützt einige Konfigurationsoptionen für Dienste nicht, mit denen ein Paket die [Dienste](../services/services.md) auf einem Computer anpassen kann. Weitere Informationen finden Sie unter [Using Services Configuration](using-services-configuration.md).

Windows Installer 4.5 unterstützt einige Features nicht, die es dem Windows Installer ermöglichen, neue Konten, Windows [Dienste,](../services/services.md)Dateien, Ordner und Registrierungsschlüssel zu schützen. Weitere Informationen finden Sie unter [Sichern von Ressourcen.](securing-resources-.md)

Windows Installer 4.5 unterstützt einige Features nicht, die es der Installation ermöglichen, alle auf dem Computer installierten Komponenten aufzuzählen und den Schlüsselpfad für die Komponente abzurufen. Weitere Informationen finden Sie unter [Aufzählen von Komponenten.](enumerating-components-.md)

 

 
