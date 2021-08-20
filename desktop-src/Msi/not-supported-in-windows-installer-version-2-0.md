---
description: Die Windows-Installer-Funktionen, -Tabellen und -Eigenschaften, die auf dieser Seite aufgeführt sind, werden von Windows Installer&\# 160;2.0 und früheren Versionen nicht unterstützt.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: Nicht unterstützt in Windows Installer 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d244dc962e65bb017dbd5fb56c7fda644b46524df7890ede7b71bf0bdf8ad66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074860"
---
# <a name="not-supported-in-windows-installer-20"></a>Nicht unterstützt in Windows Installer 2.0

Die Windows Installer-Funktionen, -Tabellen und -Eigenschaften, die auf dieser Seite aufgeführt sind, werden von Windows Installer 2.0 und früheren Versionen nicht unterstützt. Das Fehlen eines Features in dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Hauptdokumentation erfahren Sie, welche Windows Installer-Version für ein bestimmtes Feature erforderlich ist. Weitere Informationen zu anderen Windows Installer-Versionen finden Sie unter Neues [in Windows Installer.](what-s-new-in-windows-installer.md)

Windows Installer 2.0 kann unter Microsoft Windows 2000, Microsoft Windows XP oder Windows Server 2003 ausgeführt werden. Eine Liste aller Versionen des Windows Installers finden Sie unter [Veröffentlichte Versionen des Windows Installers.](released-versions-of-windows-installer.md)

Die folgenden Features werden in Windows Installer 2.0 und früheren Versionen nicht unterstützt.

[Installer-Funktionen](installer-functions.md)

-   [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
-   [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
-   [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
-   [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
-   [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
-   [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
-   [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
-   [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
-   [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
-   [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
-   [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
-   [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
-   [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
-   [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
-   [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
-   [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa)
-   [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
-   [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
-   [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
-   [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
-   [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

[Windows Installerstrukturen](installer-structures.md)

-   [**MSIPATCHSEQUENCEINFO**](/windows/win32/api/msi/ns-msi-msipatchsequenceinfoa)

[Datenbanktabellen](database-tables.md)

-   [MsiPatchCertificate](msipatchcertificate-table.md)
-   [MsiPatchSequence](msipatchsequence-table.md)
-   [MsiPatchMetadata](msipatchmetadata-table.md)

[Eigenschaften](properties.md)

-   [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**MsiPatchRemovalList**](msipatchremovallist.md)
-   [**MsiUISourceResOnly**](msiuisourceresonly.md)
-   [**MsiUIHideCancel**](msiuihidecancel.md)
-   [**MsiUIProgressOnly**](msiuiprogressonly.md)

[Systemrichtlinie](system-policy.md)

-   [DisableLUAPatching](disableluapatching.md)
-   [DisablePatchUninstall](disablepatchuninstall.md)
-   [DisableFlyWeightPatching](disableflyweightpatching.md)
-   [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md)
-   [MaxPatchCacheSize](maxpatchcachesize.md)

[Fehlercodes](error-codes.md)

-   FEHLER \_ BEIM ENTFERNEN VON \_ \_ PATCHES NICHT UNTERSTÜTZT
-   FEHLER \_ UNBEKANNTER \_ PATCH
-   FEHLER \_ PATCH \_ KEINE \_ SEQUENZ
-   FEHLER \_ BEIM ENTFERNEN VON \_ \_ PATCHES NICHT VERFÜGBAR
-   FEHLER: \_ \_ UNGÜLTIGES \_ PATCH-XML
-   FEHLERPATCH \_ \_ VERWALTETES \_ ANGEKÜNDIGTES \_ PRODUKT

Protokollierungsmodi

-   [**INSTALLLOGMODE \_ LOGONLYONERROR**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Automatisierungsschnittstelle](automation-interface.md)

-   Eigenschaften des [ **Produktobjekts**](product-object.md)

    -   [**Product.UserSid**](product-usersid.md)
    -   [**Product.Sources**](product-sources.md)
    -   [**Product.MediaDisks**](product-mediadisks.md)
    -   [**Product.FeatureState**](product-featurestate.md)
    -   [**Product.Context**](product-context.md)
    -   [**Product.InstallProperty**](product-installproperty.md)
    -   [**Product.ProductCode**](product-productcode.md)
    -   [**Product.ComponentState**](product-componentstate.md)
    -   [**Product.State**](product-state.md)
    -   [**Product.SourceListInfo**](product-sourcelistinfo.md)

-   Methoden des [ **Product-Objekts**](product-object.md)

    -   [**Product.SourceListForceResolution**](product-sourcelistforceresolution.md)
    -   [**Product.SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)
    -   [**Product.SourceListClearAll**](product-sourcelistclearall.md)
    -   [**Product.SourceListClearSource**](product-sourcelistclearsource.md)
    -   [**Product.SourceListAddSource**](product-sourcelistaddsource.md)
    -   [**Product.SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)

-   Eigenschaften des [ **Patchobjekts**](patch-object.md)

    -   [**Patch.UserSid**](patch-usersid.md)
    -   [**Patch.State**](patch-state.md)
    -   [**Patch.Sources**](patch-sources.md)
    -   [**Patch.SourceListInfo**](patch-sourcelistinfo.md)
    -   [**Patch.ProductCode**](patch-productcode.md)
    -   [**Patch.PatchProperty**](patch-patchproperty.md)
    -   [**Patch.PatchCode**](patch-patchcode.md)
    -   [**Patch.MediaDisks**](patch-mediadisks.md)
    -   [**Patch.Context**](patch-context.md)

-   Methoden des [ **Patchobjekts**](patch-object.md)

    -   [**Patch.SourceListForceResolution**](patch-sourcelistforceresolution.md)
    -   [**Patch.SourceListClearAll**](patch-sourcelistclearall.md)
    -   [**Patch.SourceListClearSource**](patch-sourcelistclearsource.md)
    -   [**Patch.SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch.SourceListAddSource**](patch-sourcelistaddsource.md)
    -   [**Patch.SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)

-   Eigenschaften des [ **Installer-Objekts**](installer-object.md)

    -   [**Installer.ProductsEx**](installer-productsex.md)
    -   [**Installer.ProductInfo**](installer-productinfo.md)
    -   [**Installer.PatchesEx**](installer-patchesex.md)

-   Methoden des [ **Installerobjekts**](installer-object.md)

    -   [**Installer.ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**Installer.ApplyPatch**](installer-applypatch.md)
    -   [**Installer.RemovePatches**](installer-removepatches.md)
    -   [**Installer.ExtractPatchXMLData**](installer-extractpatchxmldata.md)

Die folgenden Features werden auch in Windows Installer Version 2.0.2600 nicht unterstützt. Windows Die Installationsprogrammversion 2.0.2600 wurde mit Windows XP und Windows 2000 Server veröffentlicht. Die Features sind ab Windows Installer Version 2.0.3790 verfügbar, die mit Windows Server 2003 veröffentlicht wurde. Eine Liste aller Windows Installer-Versionen finden Sie unter [Veröffentlichte Versionen von Windows Installer.](released-versions-of-windows-installer.md)

[Installerfunktionen](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   MSIADVERTISEOPTIONS-INSTANZ \_
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Automatisierungsschnittstelle](automation-interface.md)

-   Methoden des [ **Installerobjekts**](installer-object.md)

    -   [**Installer.ApplyPatch**](installer-applypatch.md)
    -   [**Installer.ProductInfo**](installer-productinfo.md)

[Eigenschaften](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[Benutzerdefinierte Aktion In-Script Ausführungsoptionen](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[Fehlercodes](error-codes.md)

-   [FEHLER \_ BEI REMOTEINSTALLATION \_ \_ UNZULÄSSIG](error-codes.md)

[Computerrichtlinien](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [TransformsSecure-Richtlinie](transformssecure-policy.md)

[Befehlszeilenoptionen](command-line-options.md)

-   [/c](command-line-options.md)
-   [/n](command-line-options.md)
-   [/Lx](command-line-options.md)

[Steuerelementattribute](control-attributes.md)

-   **ImageHandle** wurde entfernt.

## <a name="notes"></a>Hinweise

Der [Standardinstaller Command-Line Optionen](standard-installer-command-line-options.md) wird von Windows Installer 2.0 nicht unterstützt. Verwenden Sie stattdessen die [befehlszeilenoptionen](command-line-options.md)für Windows Installer.

Wenn Windows Installer 2.0 ein Patchpaket installiert, werden Informationen in den Tabellen [MsiPatchSequence](msipatchsequence-table.md) oder [MsiPatchMetadata](msipatchmetadata-table.md) ignoriert. Höhere Versionen des Windows Installers können die Informationen in diesen Tabellen verwenden, um die Patchsequenzierung, -entfernung und -optimierung zu verbessern. Informationen zu verbesserten Patchfunktionen in Windows Installer finden Sie unter [Patchen von](patching.md).

Windows Installer 2.0 unterstützt keine [deinstallationsfähigen Patches.](uninstallable-patches.md) Die einzige Methode zum Entfernen bestimmter Patches aus einer Anwendung besteht darin, die gesamte gepatchte Anwendung zu deinstallieren und dann neu zu installieren, ohne patches erneut anwenden zu müssen.

Windows Installer 2.0 unterstützt keine Patchsequenzierung und installiert Patches in der Reihenfolge, in der sie dem System bereitgestellt werden, wenn [mehrere Patches installiert](installing-multiple-patches.md)werden.

Windows Installer 2.0 unterstützt nicht die Verwendung von [Benutzerkontensteuerungspatches (User Account Control, UAC),](user-account-control--uac--patching.md) um digital signierte Patches zu aktivieren, die von Benutzern ohne Administratorrechte angewendet werden können.

Windows Installer 2.0 unterstützt keine [Patchoptimierung.](patch-optimization.md) Das Patchen kann erheblich mehr Zeit in Anspruch nehmen als bei späteren versionen Windows Installers, die nur dateien aktualisieren, die vom Patch betroffen sind.

Windows Installer 2.0 unterstützt nicht [die Verwendung von Windows Installer zum Inventarisieren von Produkten und Patches.](inventory-products-and-patches-.md)

Windows Installer 2.0 unterstützt nicht das Abrufen und Ändern von Quelllisteninformationen für Windows Auf dem System installierte Installer-Anwendungen und Patches für alle Benutzer. Höhere Versionen von Windows Installer ermöglichen Administratoren das Verwalten von Quelllisten und Quelllisteneigenschaften für Netzwerk-, URL- und Medienquellen. Höhere Versionen ermöglichen Es Administratoren, Quelllisten über einen externen Prozess zu verwalten. Weitere Informationen finden Sie unter [Verwalten von Installationsquellen.](managing-installation-sources.md)

Windows Installer 2.0 unterstützt nicht die Installation mehrerer Instanzen von Produkten oder Patches ohne ein separates Installationspaket für jede Instanz. Spätere Windows Installer-Versionen können mehrere Instanzen eines Produkts mithilfe von Produktcodetransformationen und einem .msi Paket oder einem Patch installieren. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches.](installing-multiple-instances-of-products-and-patches.md)

Ab Windows XP mit Service Pack 2 (SP2) kann Windows Installer die Protokolle HTTP, HTTPS und FILE verwenden. Das Installationsprogramm unterstützt die Protokolle FTP und GOPHER nicht.

 

 



