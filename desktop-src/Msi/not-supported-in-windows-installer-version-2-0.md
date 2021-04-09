---
description: Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer&\# 160; 2.0 und früheren Versionen nicht unterstützt.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: Wird in Windows Installer 2,0 nicht unterstützt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ee09133af9ef611a93c2511d7b130b2175561b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868640"
---
# <a name="not-supported-in-windows-installer-20"></a>Wird in Windows Installer 2,0 nicht unterstützt.

Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer 2,0 und früheren Versionen nicht unterstützt. Das Fehlen eines Features aus dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Haupt Dokumentation finden Sie Informationen dazu, welche Windows Installer Version für eine bestimmte Funktion erforderlich ist. Weitere Informationen zu anderen Windows Installer Versionen finden Sie [unter What es New in Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 2,0 kann unter Microsoft Windows 2000, Microsoft Windows XP oder Windows Server 2003 ausgeführt werden. Eine Liste aller Windows Installer Versionen finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

Die folgenden Funktionen werden in Windows Installer 2,0 und früheren Versionen nicht unterstützt.

[Installer-Funktionen](installer-functions.md)

-   [**Msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
-   [**Msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
-   [**Msiapplymultiplepatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
-   [**Msienum patchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
-   [**Msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
-   [**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
-   [**Msigetproductinfoex**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
-   [**Msiqueryfeaturestateex**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
-   [**Msiquerycomponentstate**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
-   [**Msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
-   [**Msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
-   [**Msisourcelistenumschlag Quellen**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
-   [**Msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
-   [**Msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
-   [**Msisourcelistclearallex**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
-   [**Msisourcelistforceresolutionex**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa)
-   [**Msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
-   [**Msisourcelisteintinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
-   [**Msisourcelistenumschlag mediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
-   [**Msisourcelistaddmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
-   [**Msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

[Windows Installer Strukturen](installer-structures.md)

-   [**Msipatchsequenceingefo**](/windows/win32/api/msi/ns-msi-msipatchsequenceinfoa)

[Datenbanktabellen](database-tables.md)

-   [MsiPatchCertificate](msipatchcertificate-table.md)
-   [Msipatchsequenz](msipatchsequence-table.md)
-   [MsiPatchMetadata](msipatchmetadata-table.md)

[Eigenschaften](properties.md)

-   [**Msidisableluapatching**](msidisableluapatching.md)
-   [**Msienforceupgradecomponentrules**](msienforceupgradecomponentrules.md)
-   [**Msipatchremove**](msipatchremove.md)
-   [**MsiPatchRemovalList**](msipatchremovallist.md)
-   [**Msiuisourceresonly**](msiuisourceresonly.md)
-   [**Msiuihidecancel**](msiuihidecancel.md)
-   [**Msiuiprogressonly**](msiuiprogressonly.md)

[Systemrichtlinie](system-policy.md)

-   [Disableluapatching](disableluapatching.md)
-   [Disablepatchuninstall](disablepatchuninstall.md)
-   [Disableflyweightpatching](disableflyweightpatching.md)
-   [Enforceupgradecomponentrules](enforceupgradecomponentrules.md)
-   [Maxpatchcachesize](maxpatchcachesize.md)

[Fehlercodes](error-codes.md)

-   Entfernen des Fehler \_ Patches \_ \_ nicht unterstützt
-   Unbekannter Fehler beim \_ \_ Patch.
-   Fehler \_ Patch \_ keine \_ Sequenz
-   Fehler beim Entfernen des Fehler \_ Patches. \_ \_
-   Fehler \_ ungültige \_ Patch- \_ XML.
-   Fehler \_ Patch für \_ verwaltete \_ angekündigte \_ Produkte

Protokollierungs Modi

-   [**installlogmode- \_ logonlyonerror**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Automatisierungsschnittstelle](automation-interface.md)

-   Eigenschaften des [ **Product-Objekts**](product-object.md)

    -   [**Product. UserSID**](product-usersid.md)
    -   [**Product. Sources**](product-sources.md)
    -   [**Product. mediadisks**](product-mediadisks.md)
    -   [**Product. featurestate**](product-featurestate.md)
    -   [**Product. Context**](product-context.md)
    -   [**Product. InstallProperty**](product-installproperty.md)
    -   [**Product. ProductCode**](product-productcode.md)
    -   [**Product. componentstate**](product-componentstate.md)
    -   [**Product. State**](product-state.md)
    -   [**Product. sourcelistinfo**](product-sourcelistinfo.md)

-   Methoden des [ **Product-Objekts**](product-object.md)

    -   [**Product. sourcelistforceresolution**](product-sourcelistforceresolution.md)
    -   [**Product. sourcelistclearmediadisk**](product-sourcelistclearmediadisk.md)
    -   [**Product. sourcelistclearall**](product-sourcelistclearall.md)
    -   [**Product. sourcelistclearsource**](product-sourcelistclearsource.md)
    -   [**Product. sourcelistaddsource**](product-sourcelistaddsource.md)
    -   [**Product. sourcelistaddmediadisk**](product-sourcelistaddmediadisk.md)

-   Eigenschaften des [ **Patch-Objekts**](patch-object.md)

    -   [**Patch. UserSID**](patch-usersid.md)
    -   [**Patch. State**](patch-state.md)
    -   [**Patch. Quellen**](patch-sources.md)
    -   [**Patch. sourcelistinfo**](patch-sourcelistinfo.md)
    -   [**Patch. ProductCode**](patch-productcode.md)
    -   [**Patch. Patch-Eigenschaft**](patch-patchproperty.md)
    -   [**Patch. Patchcode**](patch-patchcode.md)
    -   [**Patch. mediadisks**](patch-mediadisks.md)
    -   [**Patch. Context**](patch-context.md)

-   Methoden des [ **Patch-Objekts**](patch-object.md)

    -   [**Patch. sourcelistforceresolution**](patch-sourcelistforceresolution.md)
    -   [**Patch. sourcelistclearall**](patch-sourcelistclearall.md)
    -   [**Patch. sourcelistclearsource**](patch-sourcelistclearsource.md)
    -   [**Patch. sourcelistclearmediadisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch. sourcelistaddsource**](patch-sourcelistaddsource.md)
    -   [**Patch. sourcelistaddmediadisk**](patch-sourcelistaddmediadisk.md)

-   Eigenschaften des [ **Installerobjekts**](installer-object.md)

    -   [**Installer. productsex**](installer-productsex.md)
    -   [**Installer. productinfo**](installer-productinfo.md)
    -   [**Installer. patchesex**](installer-patchesex.md)

-   Methoden des [ **Installerobjekts**](installer-object.md)

    -   [**Installer. applymultiplepatches**](installer-applymultiplepatches.md)
    -   [**Installer. Applypatch**](installer-applypatch.md)
    -   [**Installer. removepatches**](installer-removepatches.md)
    -   [**Installer. extractpatchxmldata**](installer-extractpatchxmldata.md)

Die folgenden Funktionen werden auch in Windows Installer Version 2.0.2600 nicht unterstützt. Windows Installer Version 2.0.2600 wurde mit Windows XP und Windows Server 2000 veröffentlicht. Die Features sind ab Windows Installer Version verfügbar 2.0.3790 veröffentlicht mit Windows Server 2003. Eine Liste aller Windows Installer Versionen finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

[Installer-Funktionen](installer-functions.md)

-   [**Msiankündigen-productex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   msiankündigen-options \_ Instanz
-   [**Msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**Msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Automatisierungsschnittstelle](automation-interface.md)

-   Methoden des [ **Installerobjekts**](installer-object.md)

    -   [**Installer. Applypatch**](installer-applypatch.md)
    -   [**Installer. productinfo**](installer-productinfo.md)

[Eigenschaften](properties.md)

-   [**Msinewinstance**](msinewinstance.md)
-   [**Msiinstanceguid**](msiinstanceguid.md)
-   [**Msintsuitewebserver**](msintsuitewebserver.md)

[Benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md)

-   [**msidbcustomaktiontypetsaware**](custom-action-in-script-execution-options.md)

[Fehlercodes](error-codes.md)

-   [Fehler beim \_ Installieren der \_ Remote Installation. \_](error-codes.md)

[Computer Richtlinien](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [Transformssecure-Richtlinie](transformssecure-policy.md)

[Befehlszeilenoptionen](command-line-options.md)

-   [/c](command-line-options.md)
-   [/n](command-line-options.md)
-   [/Lx](command-line-options.md)

[Steuerelement Attribute](control-attributes.md)

-   **Imagehandle** wurde entfernt.

## <a name="notes"></a>Notizen

Die [Standard Optionen](standard-installer-command-line-options.md) für das Installationsprogramm Command-Line werden von Windows Installer 2,0 nicht unterstützt. Verwenden Sie stattdessen die Windows Installer [Befehlszeilenoptionen](command-line-options.md).

Wenn Windows Installer 2,0 ein Patchpaket installiert, werden Informationen in den Tabellen [msipatchsequence](msipatchsequence-table.md) oder [MsiPatchMetadata](msipatchmetadata-table.md) ignoriert. Spätere Versionen des Windows Installer können die Informationen in diesen Tabellen verwenden, um die Patchsequenzierung, das Entfernen und die Optimierung zu verbessern. Informationen zu verbesserten Funktionen für das Patchen in Windows Installer finden Sie unter [Patchen](patching.md).

Windows Installer 2,0 unterstützt keine nicht [installierbaren Patches](uninstallable-patches.md) , und die einzige Methode, bestimmte Patches aus einer Anwendung zu entfernen, besteht darin, die gesamte gepatchte Anwendung zu deinstallieren und dann erneut zu installieren, ohne dass Patches entfernt werden müssen.

Windows Installer 2,0 unterstützt keine Patchsequenzierung und installiert Patches in der Reihenfolge, in der Sie dem System bei der [Installation mehrerer Patches](installing-multiple-patches.md)bereitgestellt werden.

Windows Installer 2,0 bietet keine Unterstützung für das [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) , um Digital signierte Patches zu aktivieren, die von Benutzern ohne Administratorrechte angewendet werden können.

Windows Installer 2,0 bietet keine Unterstützung für die [patchoptimierung](patch-optimization.md). Das Patchen kann deutlich mehr Zeit in Anspruch nehmen als bei späteren Windows Installer Versionen, die nur die vom Patch betroffenen Dateien aktualisieren.

Windows Installer 2,0 unterstützt [die Verwendung von Windows Installer nicht zum Inventarisieren von Produkten und Patches](inventory-products-and-patches-.md).

Windows Installer 2,0 unterstützt nicht das Abrufen und Ändern von Quell Listen Informationen für Windows Installer Anwendungen und Patches, die auf dem System für alle Benutzer installiert wurden. Spätere Versionen von Windows Installer ermöglichen Administratoren das Verwalten von Quell Listen und Quell Listen Eigenschaften für Netzwerk-, URL-und Medienquellen. Spätere Versionen ermöglichen es Administratoren, Quell Listen aus einem externen Prozess zu verwalten. Weitere Informationen finden Sie unter [Verwalten von Installations Quellen](managing-installation-sources.md).

Windows Installer 2,0 unterstützt nicht die Installation mehrerer Instanzen von Produkten oder Patches ohne ein separates Installationspaket für jede Instanz. Spätere Windows Installer Versionen können mithilfe von Produktcode Transformationen und einem MSI-Paket oder einem Patch mehrere Instanzen eines Produkts installieren. Weitere Informationen finden Sie [unter Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md).

Ab Windows XP mit Service Pack 2 (SP2) können Windows Installer http-, HTTPS-und Datei Protokolle verwenden. Das Installationsprogramm unterstützt das FTP-und das Gopher-Protokoll nicht.

 

 



