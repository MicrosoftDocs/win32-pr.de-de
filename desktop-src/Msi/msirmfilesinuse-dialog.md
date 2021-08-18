---
description: Das Dialogfeld MsiRMFilesInUse kann erstellt werden, um eine Liste von Prozessen anzuzeigen, die derzeit Dateien ausführen, die von der Installation überschrieben oder gelöscht werden müssen.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Dialogfeld "MsiRMFilesInUse"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04aa3167609693135e2d3196fef0495d5244fe44f1a6e7d95d11f999efe51a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012888"
---
# <a name="msirmfilesinuse-dialog"></a>Dialogfeld "MsiRMFilesInUse"

Das Dialogfeld MsiRMFilesInUse kann erstellt werden, um eine Liste von Prozessen anzuzeigen, die derzeit Dateien ausführen, die von der Installation überschrieben oder gelöscht werden müssen. Der Benutzer kann zwischen den Optionen "Anwendungen automatisch schließen und neu starten" oder "Anwendungen nicht schließen" auswählen. (Ein Neustart ist erforderlich.) Wenn der Benutzer die Option "Anwendungen automatisch schließen und neu starten" auswählt, kann ein Schaltflächen-Steuerelement in diesem Dialogfeld erstellt werden, um das RMShutdownAndRestart-Steuerelementereignis zu veröffentlichen, und der [Neustart-Manager](../rstmgr/restart-manager-portal.md) kann die Anwendungen schließen und am Ende der Installation neu starten. Dies kann dazu beitragen, dass der Computer nicht mehr neu gestartet werden muss. Weitere Informationen finden Sie unter [Systemneustarts.](system-reboots.md)

Das Dialogfeld **MsiRMFilesInUse** wird während einer Installation nur angezeigt, wenn alle folgenden Punkte zutreffen. Wenn eine dieser Optionen false ist, ignoriert der Windows Installer das Dialogfeld **MsiRMFilesInUse.**

-   Eine Windows Installer-Version, die nicht älter als Version 4.0 ist, und ein Betriebssystem, das nicht älter als Windows Vista oder Windows Server 2008 ist, führt die Installation aus.
-   Die Benutzeroberflächenebene "Vollständige [Benutzeroberfläche"](user-interface-levels.md) wird verwendet.
-   Interaktionen mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) wurden nicht durch die [**MSIRESTARTMANAGERCONTROL-Eigenschaft**](msirestartmanagercontrol.md) oder die [DisableAutomaticApplicationShutdown-Richtlinie](disableautomaticapplicationshutdown.md) deaktiviert.
-   Das Dialogfeld **MsiRMFilesInUse** ist im Installationspaket vorhanden.
-   Alle Aufrufe des Windows Installers an den [Neustart-Manager](../rstmgr/restart-manager-portal.md) sind erfolgreich.

Dieses Dialogfeld wird nach Bedarf von der [InstallValidate-Aktion](installvalidate-action.md)erstellt.

 

 
