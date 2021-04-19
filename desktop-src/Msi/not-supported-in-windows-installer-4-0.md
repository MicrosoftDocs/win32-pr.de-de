---
description: Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer&\# 160; 4.0 und früheren Versionen nicht unterstützt.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: Wird in Windows Installer 4,0 nicht unterstützt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4307422c71976057948759078dc321e38dc543b7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106364308"
---
# <a name="not-supported-in-windows-installer-40"></a>Wird in Windows Installer 4,0 nicht unterstützt.

Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer 4,0 und früheren Versionen nicht unterstützt. Das Fehlen eines Features aus dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Haupt Dokumentation finden Sie Informationen dazu, welche Windows Installer Version für eine bestimmte Funktion erforderlich ist. Weitere Informationen zu anderen Windows Installer Versionen finden Sie [unter What es New in Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 4,0 ist für Microsoft Windows Server 2008 und Windows Vista verfügbar. Eine vollständige Liste aller Windows Installer Versionen und verteilbaren Komponenten finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

Die folgenden Funktionen werden in Windows Installer 4,0 und früheren Versionen nicht unterstützt.

[Installer-Funktionen](installer-functions.md)

-   [**Msibegintransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**Msiendtransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**Msijointransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[Eigenschaften](properties.md)

-   [**Msidisableeeui**](msidisableeeui.md)
-   [**Msiuninstallablösung dedcomponents**](msiuninstallsupersededcomponents.md)

[Datenbanktabellen](database-tables.md)

-   [Msiembeddecodchainer-Tabelle](msiembeddedchainer-table.md)
-   [Msiembeddedui-Tabelle](msiembeddedui-table.md)
-   [Msipackagecertificate-Tabelle](msipackagecertificate-table.md)
-   [Komponenten Tabelle](component-table.md)
- **msidbcomponentattributesuninstallonablösung**  
    **msidbcomponentattributesshared**  
    
-   [CustomAction](customaction-table.md) Spalte "extendedtype"  
    

[Option zum Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md)



[Msitransformview\<PatchGUID\>](msitransformview.md)  

**msidbcustomaktiontypepatchuninstall**  


[Systemrichtlinie](system-policy.md)

-   [Disablesharedcomponent](disablesharedcomponent.md)
-   [Msidisableembeddedui](msidisableembeddedui.md)

Rückruf Funktionsprototypen

-   *Embeddeduihandler*
-   *Initializeembeddedui*
-   *Shutdownembeddedui*

[Interne Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) überprüft, ob keine Komponente sowohl das **msidbcomponentattributespermanent** -Attribut als auch das **msidbcomponentattributesuninstallonabgelöst** -Attribut aufweist.

## <a name="notes"></a>Notizen

Windows Installer 4,0 kann nicht [mehrere Paketinstallationen](multiple-package-installations.md) mithilfe der [*Transaktionsverarbeitung*](t-gly.md)durchführen.

Wenn Sie Windows Installer 4,0 oder frühere Versionen des Installers verwenden, kann es bei kleinen Updates und geringfügigen Upgrades zu Fehlern kommen, wenn die [enforceupgradecomponentrules](enforceupgradecomponentrules.md) -Richtlinie oder die [**msienforceupgradecomponentrules**](msienforceupgradecomponentrules.md) -Eigenschaft verwendet wird, da das Update eine Komponente entfernt.

Eine benutzerdefinierte Benutzeroberfläche kann nicht mit der unter [Verwendung einer eingebetteten](using-an-embedded-ui.md)Benutzeroberfläche beschriebenen Methode in das Windows Installer Paket eingebettet werden.

 

 



