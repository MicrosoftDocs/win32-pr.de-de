---
description: Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer&\# 160; 3.1 und früheren Versionen nicht unterstützt.
ms.assetid: fbf75dbe-3fa1-424b-83bb-cfd0b179107c
title: Wird in Windows Installer 3,1 nicht unterstützt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a221d80f56c5737cc5ae92a040a005ae42449e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362972"
---
# <a name="not-supported-in-windows-installer-31"></a>Wird in Windows Installer 3,1 nicht unterstützt.

Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer 3,1 und früheren Versionen nicht unterstützt. Das Fehlen eines Features aus dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Haupt Dokumentation finden Sie Informationen dazu, welche Windows Installer Version für eine bestimmte Funktion erforderlich ist. Weitere Informationen zu anderen Windows Installer Versionen finden Sie [unter What es New in Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 3,1 ist für Windows Server 2003, Windows XP oder Windows 2000 verfügbar. Eine Liste aller Windows Installer Versionen und verteilbaren Komponenten finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

Die folgenden Funktionen werden in Windows Installer 3,1 und früheren Versionen nicht unterstützt.

[Installer-Funktionen](installer-functions.md)

-   [**Msigetpatchfilelist**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)

[Eigenschaften](properties.md)

-   [**Msiarpsettingsidentifier**](msiarpsettingsidentifier.md)
-   [**Msideploymentcompliance**](msideploymentcompliant.md)
-   [**Msidisablermrestart**](msidisablermrestart.md)
-   [**Msilogfileloation**](msilogfilelocation.md)
-   [**MsiLogging**](msilogging.md)
-   [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
-   [**Msirestartmanagersessionkey**](msirestartmanagersessionkey.md)
-   [**Msirmshutdown**](msirmshutdown.md)
-   [**Msirunningelevated**](msirunningelevated-.md)
-   [**Msisystemrebootpending**](msisystemrebootpending.md)
-   [**Msitabletpc**](msitabletpc.md)
-   [**Msiuserealadminerkennungs**](msiuserealadmindetection.md)

[Eigenschaften von Zusammenfassungs Informationen](summary-information-stream-reference.md)

-   Die " [**Word Count Summary**](word-count-summary.md) "-Eigenschaft weist neue Flagbits auf, um anzugeben, ob die Installation des Pakets erhöhte Rechte erfordert.

[Systemrichtlinie](system-policy.md)

-   [Disableautomaticapplicationshutdown](disableautomaticapplicationshutdown.md)
-   [Disableloggingfrompackage](disableloggingfrompackage.md)

[Datenbanktabellen](database-tables.md)

-   [Verknüpfungs Tabelle](shortcut-table.md)

    Neue Spalten: displayresourcedll, displayresourceid, descriptionresourcedll und descriptionresourceid

[Dialog Felder](dialog-boxes.md)

-   [Dialog Feld "msirmfilesinuse"](msirmfilesinuse-dialog.md)

[Steuerelement Attribute](control-attributes.md)

-   [Elevationshield](elevationshield-attribute.md)

[ControlEvents](control-events.md)

-   [Rmshutdownandrestart](rmshutdownandrestart-controlevent.md)

[Externe UI-Nachrichten Typen](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

-   installlogmode \_ rmfilesinuse

[Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)

-   **msidbcomponentattributesdisableregistryreflection** -Attribut in der [Component-Tabelle](component-table.md)

[Automatisierungsschnittstelle](automation-interface.md)

-   Methoden des [ **Installerobjekts**](installer-object.md)

    -   [**Installer. Werbung**](installer-advertiseproduct.md)
    -   [**Installer. Werbung**](installer-advertisescript.md)
    -   [**Installer. kreatewerbung**](installer-createadvertisescript.md)
    -   [**Installer. providebug Assembly**](installer-provideassembly.md)

-   Eigenschaften des [ **Installerobjekts**](installer-object.md)

    -   [**Datei "Installer. PATCHFILES"**](installer-patchfiles.md)
    -   [**Installer. productelevated**](installer-productelevated.md)
    -   [**Installer. productinfofromscript**](installer-productinfofromscript.md)

## <a name="notes"></a>Notizen

Der Windows Installer-Dienst muss unter Windows Vista ausgeführt werden, um das Patchen von [Neustart-Manager](../rstmgr/restart-manager-portal.md), [*Benutzerkontensteuerung*](u-gly.md)und [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)zu ermöglichen. Weitere Informationen finden [Sie unter Verwenden von Windows Installer mit dem Neustart-Manager](using-windows-installer-with-restart-manager.md) und Verwenden von [Windows Installer mit UAC](using-windows-installer-with-uac.md) und [Benutzerkontensteuerung (User Account Control, UAC) Patching](user-account-control--uac--patching.md).

Windows Installer 3,1 unterstützt den Windows-Datei Schutz (WFP) und unterstützt Windows-Ressourcenschutz (WRP) nicht. WRP in Windows Server 2008 und Windows Vista ersetzt WFP in Windows Server 2003, Windows XP und Windows 2000. Weitere Informationen zu Windows Installer und WFP finden [Sie unter Verwenden von Windows Installer und Windows-Ressourcenschutz](windows-resource-protection-on-windows-vista.md).

 

 
