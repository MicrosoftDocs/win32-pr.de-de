---
description: Da die Benutzerkontensteuerung (User Account Control, UAC) in Windows Vista Berechtigungen während einer Installation einschränkt, sollten Entwickler von Windows Installer Paketen nicht davon ausgehen, dass Ihre Installation immer Zugriff auf alle Teile des Systems hat.
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: Richtlinien für Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db228c2dff443d421ddc089074f0fcce6ae93e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866323"
---
# <a name="guidelines-for-packages"></a>Richtlinien für Pakete

Da die [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) in Windows Vista Berechtigungen während einer Installation einschränkt, sollten Entwickler von Windows Installer Paketen nicht davon ausgehen, dass Ihre Installation immer Zugriff auf alle Teile des Systems hat.

Ein Installer-Paket, das über [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page) erfolgreich für Standardbenutzer bereitgestellt werden kann, sollte in den meisten Fällen auch mit UAC in Windows Vista funktionieren. Ausnahmen können auftreten, wenn die [Tabelle "InstallUISequence](installuisequence-table.md) " die [Aktion "LaunchConditions](launchconditions-action.md) " enthält oder die [Tabelle "LaunchCondition](launchcondition-table.md) " eine Bedingung enthält, die auf der [privilegierten Eigenschaft](privileged.md)basiert. Entwickler von Windows Installer Paketen sollten daher die folgenden Richtlinien befolgen, um sicherzustellen, dass Ihr Paket mit UAC und Windows Vista funktioniert.

-   Wenn Sie eine [*Installations Kontext*](i-gly.md) Bedingung mit einer Aktion in der [Tabelle InstallUISequence](installuisequence-table.md)einschließen, verwenden Sie eine Bedingungs Anweisung, die auf der [privilegierten Eigenschaft](privileged.md)basiert. Verwenden Sie keine Bedingung, die auf der [**AdminUser**](adminuser.md) -Eigenschaft basiert.
-   Wenn Sie den Installations Kontext mit den Installations Startbedingungen einschließen, verwenden Sie den [benutzerdefinierten Aktionstyp 19](custom-action-type-19.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) , und legen Sie die benutzerdefinierte Aktion auf die [privilegierte Eigenschaft](privileged.md)fest. Verwenden Sie keine Aktion in der [LaunchCondition-Tabelle](launchcondition-table.md) mit einer Bedingung, die auf der [AdminUser-Eigenschaft](adminuser.md) oder der privilegierten Eigenschaft basiert.
-   Um die Systemkonfiguration zu lesen oder zu ändern, verwenden Sie eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md). Verwenden Sie keine benutzerdefinierten Aktionen für die sofortige Ausführung in der [Tabelle InstallUISequence](installuisequence-table.md) , um die Systemkonfiguration zu ändern.
-   Um Teile des Systems zu ändern, die Nichtbenutzer spezifisch sind, verwenden Sie eine verzögerte benutzerdefinierte Aktion in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md). Sie sollten das msidbcustomaction typoidentitäts Ate-Bit in den benutzerdefinierten Aktionstyp einschließen.
-   Lassen Sie Bit 3 aus dem Wert der Eigenschaft [**Wort Zähl**](word-count-summary.md) Zusammenfassung aus, um anzugeben, dass das Paket erhöht werden kann. Fügen Sie dieses Bit nicht ein, es sei denn, für die Installation dieses Pakets sind erhöhte Rechte erforderlich.
-   Fügen Sie ein Manifest mit der angeforderten Ausführungs Ebene der Anwendung ein.
-   Fügen Sie ein Zertifikat in die [MsiPatchCertificate](msipatchcertificate-table.md) -Tabelle des ursprünglichen Pakets ein, und Signieren Sie alle Patches mit demselben Zertifikat.
-   Wenn für die Installation eines Windows Installer Pakets erhöhte Rechte erforderlich sind, sollte der Autor des Pakets das [elevationshield](elevationshield-attribute.md) -Attribut für das [PUSHBUTTON-Steuer](pushbutton-control.md) Element enthalten, das zum Starten der Installation verwendet wird. Dadurch wird der Benutzer gewarnt, dass durch Klicken auf die Schaltfläche das UAC-Dialogfeld zum Fortsetzen der Installation auf die Schaltfläche angezeigt wird.
-   Legen Sie für die Eigenschaft [**msideploymentcompliance**](msideploymentcompliant.md) den Wert 1 fest, um den Windows Installer anzugeben, dass das Paket erstellt und getestet wurde, um die UAC in Windows Vista einzuhalten. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt das Installationsprogramm, ob das Paket UAC einhält.

Außerhalb [Gruppenrichtlinie](/previous-versions/windows/desktop/Policy/group-policy-start-page)kann die folgende Überprüfung der UAC-Kompatibilität unter Windows XP verwendet werden.

**So überprüfen Sie die UAC-Konformität außerhalb der Gruppenrichtlinie**

1.  Melden Sie sich als Administrator beim Computer an.
2.  Ankündigen Sie das Paket für eine Installation pro Computer:

    **msiexec/JM** *package.msi*

3.  Melden Sie sich vom Computer ab.
4.  Melden Sie sich als Standardbenutzer beim Computer an.
5.  Versuch der Installation des angekündigten Pakets:

    **msiexec/i** *package.msi*

6.  In den meisten Fällen ist das Paket mit UAC kompatibel, wenn die Installation erfolgreich ist.
7.  Legen Sie die [**msideploymentcompliance**](msideploymentcompliant.md) -Eigenschaft im Paket auf 1 fest.
8.  Testen Sie die korrekte Installation des Pakets mithilfe von Windows Vista.

 

 
