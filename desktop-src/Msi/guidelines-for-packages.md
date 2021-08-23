---
description: Da die Benutzerkontensteuerung (User Account Control, UAC) in Windows Vista Berechtigungen während einer Installation einschränkt, sollten Entwickler von Windows Installer-Paketen nicht davon ausgehen, dass ihre Installation immer Zugriff auf alle Teile des Systems hat.
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: Richtlinien für Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930cb97cd2bb01a2bd69c5950a7e054c73d355e534ab67c812bcde44b7495b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649320"
---
# <a name="guidelines-for-packages"></a>Richtlinien für Pakete

Da die Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) in Windows Vista berechtigungen während einer Installation einschränkt, sollten Entwickler von Windows Installer-Paketen nicht davon ausgehen, dass ihre Installation immer Zugriff auf alle Teile des Systems hat.

Ein Installationspaket, das über [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page) erfolgreich für Standardbenutzer bereitgestellt werden kann, sollte in den meisten Fällen auch mit UAC in Windows Vista funktionieren. Ausnahmen können auftreten, wenn die [Tabelle InstallUISequence](installuisequence-table.md) die [LaunchConditions-Aktion](launchconditions-action.md) enthält oder die [LaunchCondition-Tabelle](launchcondition-table.md) eine Bedingung enthält, die auf der [Privileged-Eigenschaft](privileged.md)basiert. Windows Entwickler von Installerpaketen sollten daher die folgenden Richtlinien einhalten, um sicherzustellen, dass ihr Paket mit UAC und Windows Vista funktioniert.

-   Wenn Sie eine [*Installationskontextbedingung*](i-gly.md) mit einer Aktion in die [Tabelle InstallUISequence](installuisequence-table.md)einschließen, verwenden Sie eine bedingte Anweisung, die auf der [Privileged-Eigenschaft](privileged.md)basiert. Verwenden Sie keine Bedingung, die auf der [**AdminUser-Eigenschaft**](adminuser.md) basiert.
-   Wenn Sie den Installationskontext mit den Startbedingungen der Installation einschließen, verwenden Sie in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) den [benutzerdefinierten Aktionstyp 19,](custom-action-type-19.md) und machen Sie die benutzerdefinierte Aktion von der [Privileged-Eigenschaft](privileged.md)abhängig. Verwenden Sie keine Aktion in der [LaunchCondition-Tabelle](launchcondition-table.md) mit einer Bedingung, die auf der [AdminUser-Eigenschaft](adminuser.md) oder der Privileged-Eigenschaft basiert.
-   Um die Systemkonfiguration zu lesen oder zu ändern, verwenden Sie eine benutzerdefinierte Aktion zur [verzögerten Ausführung](deferred-execution-custom-actions.md) in der Tabelle [InstallExecuteSequence.](installexecutesequence-table.md) Verwenden Sie keine benutzerdefinierten Aktionen zur sofortigen Ausführung in der [Tabelle InstallUISequence,](installuisequence-table.md) um die Systemkonfiguration zu ändern.
-   Um Teile des Systems zu ändern, die nicht benutzerspezifisch sind, verwenden Sie eine verzögerte benutzerdefinierte Aktion in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md). Sie sollten das Bit msidbCustomActionTypeNoImpersonate in den benutzerdefinierten Aktionstyp einschließen.
-   Lassen Sie Bit 3 aus dem Wert der [**Word Count**](word-count-summary.md) Summary-Eigenschaft aus, um anzugeben, dass für das Paket erhöhte Rechte erforderlich sein können. Schließen Sie dieses Bit nur ein, wenn für die Installation dieses Pakets erhöhte Rechte erforderlich sind.
-   Schließen Sie ein Manifest mit der angeforderten Ausführungsebene der Anwendung ein.
-   Fügen Sie ein Zertifikat in die [MsiPatchCertificate-Tabelle](msipatchcertificate-table.md) des ursprünglichen Pakets ein, und signieren Sie alle Patches mit demselben Zertifikat.
-   Wenn zum Installieren eines Windows Installer-Pakets erhöhte Rechte erforderlich sind, sollte der Ersteller des Pakets das [ElevationShield-Attribut](elevationshield-attribute.md) für das [PushButton-Steuerelement](pushbutton-control.md) enthalten, das zum Starten der Installation verwendet wird. Dadurch wird der Benutzer benachrichtigt, dass durch Klicken auf die Schaltfläche das Dialogfeld für die Benutzerkontenverwaltung angezeigt wird, in dem die Administratorautorisierung angefordert wird, um die Installation fortzusetzen.
-   Legen Sie die [**MSIDEPLOYMENTCOMPLIANT-Eigenschaft**](msideploymentcompliant.md) auf 1 fest, um dem Windows Installer anzugeben, dass das Paket erstellt und getestet wurde, um die UAC in Windows Vista zu erfüllen. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt das Installationsprogramm, ob das Paket der UAC entspricht.

Außerhalb von [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)kann die folgende Überprüfung auf UAC-Konformität auf Windows XP verwendet werden.

**So überprüfen Sie, ob die UAC-Konformität außerhalb von Gruppenrichtlinie**

1.  Melden Sie sich als Administrator beim Computer an.
2.  Kündigen Sie das Paket für eine Computerinstallation an:

    **msiexec /jm** *package.msi*

3.  Melden Sie sich vom Computer ab.
4.  Melden Sie sich als Standardbenutzer beim Computer an.
5.  Versuchen Sie, das angekündigte Paket zu installieren:

    **msiexec /i** *package.msi*

6.  In den meisten Fällen ist das Paket UAC-kompatibel, wenn die Installation erfolgreich war.
7.  Legen Sie die [**MSIDEPLOYMENTCOMPLIANT-Eigenschaft**](msideploymentcompliant.md) im Paket auf 1 fest.
8.  Testen Sie mit Windows Vista, dass das Paket ordnungsgemäß installiert wurde.

 

 
