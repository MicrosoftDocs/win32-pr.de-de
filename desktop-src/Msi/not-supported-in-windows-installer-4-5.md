---
description: Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer&\# 160; 4.5 und früheren Versionen nicht unterstützt.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: Wird in Windows Installer 4,5 nicht unterstützt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d1d1b3039c4e51c7233f98ee2e41afb308a822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754217"
---
# <a name="not-supported-in-windows-installer-45"></a>Wird in Windows Installer 4,5 nicht unterstützt.

Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer 4,5 und früheren Versionen nicht unterstützt. Das Fehlen eines Features aus dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Haupt Dokumentation finden Sie Informationen dazu, welche Windows Installer Version für eine bestimmte Funktion erforderlich ist. Weitere Informationen zu anderen Windows Installer Versionen finden Sie [unter What es New in Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 4,5 ist als verteilbare Komponente für Windows Server 2008, Windows Vista mit Service Pack 1 (SP1), Windows XP mit Service Pack 2 (SP2) und höher und Windows Server 2003 mit Service Pack 1 (SP1) und höher verfügbar. Eine vollständige Liste aller Windows Installer Versionen und verteilbaren Komponenten finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

Die folgenden Funktionen werden in Windows Installer 4,5 und früheren Versionen nicht unterstützt.

[Standard Aktionen](standard-actions.md)

-   [Msikonfigurireservices](msiconfigureservices-action.md)

[Installer-Funktionen](installer-functions.md)

-   [**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**Msienumschlag clientsex**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**Msigetcomponentpathex**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[Spaltendatentypen](column-data-types.md)

-   [**Formattedsddltext**](formattedsddltext.md)

[Eigenschaften](properties.md)

-   [**Msifastinstall**](msifastinstall.md)
-   [**Msiinstallperuser**](msiinstallperuser.md)

[Datenbanktabellen](database-tables.md)

-   [Msiserviceconfig-Tabelle](msiserviceconfig-table.md)
-   [Msiserviceconfigfailureactions-Tabelle](msiserviceconfigfailureactions-table.md)
-   [Msishortcutproperty-Tabelle](msishortcutproperty-table.md)
-   [Msilockpermissionsex-Tabelle](msilockpermissionsex-table.md)

[ControlEvents](control-events.md)

-   [Msiprint ControlEvent](msiprint-controlevent.md)
-   [Msilaunchapp ControlEvent](msilaunchapp-controlevent.md)

[Steuerelemente](controls.md)

-   [Hyperlink-Steuerelement](hyperlink-control.md)
-   Unterstützung von [Bitmap-Steuer](bitmap-control.md) Elementen von WIC-Bild Dateiformaten

[Interne Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Automatisierungsschnittstelle](automation-interface.md)

-   Eigenschaften des [ **Installerobjekts**](installer-object.md)

    -   [**Installer. clientsex**](installer-clientsex.md)
    -   [**Installer. componentsex**](installer-componentsex.md)
    -   [**Installer. componentpathex**](installer-componentpathex.md)

-   Eigenschaften des [ **Komponenten Objekts**](components.md)

    -   [**Component. componentcode**](component-componentcode.md)
    -   [**Component. UserSID**](component-usersid.md)
    -   [**Component. Context**](component-context.md)

-   Eigenschaften des [ **Client Objekts**](client.md)

    -   [**Client. ProductCode**](client-productcode.md)
    -   [**Client. componentcode**](client-componentcode.md)
    -   [**Client. UserSID**](client-usersid.md)
    -   [**Client. Context**](client-context.md)

-   Eigenschaften des [**ComponentInfo**](componentinfo.md) -Objekts

    -   [**ComponentInfo. componentcode**](componentinfo-componentcode.md)
    -   [**ComponentInfo. Path**](componentinfo-path.md)
    -   [**ComponentInfo. State**](componentinfo-state.md)

## <a name="notes"></a>Notizen

Windows Installer 4,5 bietet keine Unterstützung für einige Features, mit denen ein einzelnes Installationspaket entweder im Computer-oder benutzerspezifischen Installations Kontext installiert werden kann. Weitere Informationen finden Sie unter [Erstellen eines einzelnen Pakets](single-package-authoring.md).

In Windows Installer 4,5 werden einige Konfigurationsoptionen für Dienste nicht unterstützt, mit denen ein Paket die [Dienste](../services/services.md) auf einem Computer anpassen kann. Weitere Informationen finden Sie unter [Verwenden der Dienst Konfiguration](using-services-configuration.md).

Windows Installer 4,5 bietet keine Unterstützung für einige Features, die es dem Windows Installer ermöglichen, neue Konten, Windows- [Dienste](../services/services.md), Dateien, Ordner und Registrierungsschlüssel zu sichern. Weitere Informationen finden Sie unter [Sichern von Ressourcen](securing-resources-.md).

Windows Installer 4,5 bietet keine Unterstützung für einige Features, mit denen die Installation alle auf dem Computer installierten Komponenten aufzählen und den Schlüssel Pfad für die Komponente abrufen kann. Weitere Informationen finden Sie unter [Enumerieren von Komponenten](enumerating-components-.md).

 

 
