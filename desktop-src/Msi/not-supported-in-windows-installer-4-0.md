---
description: Die auf dieser Seite aufgeführten Windows Installer-Funktionen, -Tabellen und -Eigenschaften werden von Windows Installer&\# 160;4.0 und früheren Versionen nicht unterstützt.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: Nicht unterstützt in Windows Installer 4.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444040fca716b6bd64c8598d2d2e36013fe19cc62971483507756a66f3e961bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558800"
---
# <a name="not-supported-in-windows-installer-40"></a>Nicht unterstützt in Windows Installer 4.0

Die auf dieser Seite aufgeführten Windows Installer-Funktionen, -Tabellen und -Eigenschaften werden von Windows Installer 4.0 und früheren Versionen nicht unterstützt. Das Fehlen eines Features in dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Hauptdokumentation erfahren Sie, welche Windows Installer-Version für ein bestimmtes Feature erforderlich ist. Informationen zu anderen Windows Installer-Versionen finden Sie unter [Neuerungen in Windows Installer.](what-s-new-in-windows-installer.md)

Windows Installer 4.0 ist für Microsoft Windows Server 2008 und Windows Vista verfügbar. Eine vollständige Liste aller Windows Installer-Versionen und verteilbaren Versionen finden Sie unter [Veröffentlichte Versionen von Windows Installer.](released-versions-of-windows-installer.md)

Die folgenden Features werden in Windows Installer 4.0 und früheren Versionen nicht unterstützt.

[Installerfunktionen](installer-functions.md)

-   [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[Eigenschaften](properties.md)

-   [**MSIDISABLEEEUI**](msidisableeeui.md)
-   [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)

[Datenbanktabellen](database-tables.md)

-   [MsiEmbeddedChainer-Tabelle](msiembeddedchainer-table.md)
-   [MsiEmbeddedUI-Tabelle](msiembeddedui-table.md)
-   [MsiPackageCertificate-Tabelle](msipackagecertificate-table.md)
-   [Komponententabelle](component-table.md)
- **msidbComponentAttributesUninstallOnSupersedence**  
    **msidbComponentAttributesShared**  
    
-   [CustomAction](customaction-table.md) ExtendedType-Spalte  
    

[Deinstallationsoption für benutzerdefinierte Aktionspatches](custom-action-patch-uninstall-option.md)



[MsiTransformView\<PatchGUID\>](msitransformview.md)  

**msidbCustomActionTypePatchUninstall**  


[Systemrichtlinie](system-policy.md)

-   [DisableSharedComponent](disablesharedcomponent.md)
-   [MsiDisableEmbeddedUI](msidisableembeddedui.md)

Rückruffunktionsprototypen

-   *EmbeddedUIHandler*
-   *InitializeEmbeddedUI*
-   *ShutdownEmbeddedUI*

[Interne Konsistenzauswertungen – ICEs](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) überprüft, ob keine Komponente über die Attribute **msidbComponentAttributesPermanent** und **msidbComponentAttributesUninstallOnSupersedence verfügt.**

## <a name="notes"></a>Hinweise

Windows Installer 4.0 kann [mehrere Paketinstallationen](multiple-package-installations.md) nicht mithilfe der [*Transaktionsverarbeitung*](t-gly.md)ausführen.

Mit Windows Installer 4.0 oder früheren Versionen des Installationsprogramms können kleine Updates und kleinere Upgrades fehlschlagen, wenn die [EnforceUpgradeComponentRules-Richtlinie](enforceupgradecomponentrules.md) oder die [**MSIENFORCEUPGRADECOMPONENTRULES-Eigenschaft**](msienforceupgradecomponentrules.md) verwendet wird, da das Update eine Komponente entfernt.

Eine benutzerdefinierte Benutzeroberfläche kann nicht mithilfe der unter Verwenden [einer eingebetteten Benutzeroberfläche](using-an-embedded-ui.md)beschriebenen Methode in das paket Windows Installer eingebettet werden.

 

 



