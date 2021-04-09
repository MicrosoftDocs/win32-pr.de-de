---
description: Das Dialog Feld msirmfilesinuse kann erstellt werden, um eine Liste der Prozesse anzuzeigen, die derzeit Dateien ausführen, die bei der Installation überschrieben oder gelöscht werden müssen.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Dialog Feld "msirmfilesinuse"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bba73cab51f4b3d8321b15001dbb72c638176b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960761"
---
# <a name="msirmfilesinuse-dialog"></a>Dialog Feld "msirmfilesinuse"

Das Dialog Feld msirmfilesinuse kann erstellt werden, um eine Liste der Prozesse anzuzeigen, die derzeit Dateien ausführen, die bei der Installation überschrieben oder gelöscht werden müssen. Der Benutzer kann zwischen Optionen zum automatischen Schließen von Anwendungen und Neustarten oder "Anwendungen nicht schließen" auswählen. (Ein Neustart ist erforderlich.) Wenn der Benutzer die Option "Anwendungen automatisch schließen und neu starten" auswählt, kann ein Push-Schaltflächen-Steuerelement in diesem Dialogfeld erstellt werden, um das rmshutdownandrestart-Steuerungs Ereignis zu veröffentlichen, und der [Neustart-Manager](../rstmgr/restart-manager-portal.md) kann die Anwendungen schließen und am Ende der Installation neu starten. Dadurch kann der Computer nicht neu gestartet werden. Weitere Informationen finden Sie unter [System Neustarts](system-reboots.md).

Das Dialogfeld **msirmfilesinuse** wird nur während einer Installation angezeigt, wenn Folgendes zutrifft: Wenn eine dieser beiden Typen false ist, wird das Dialogfeld **msirmfilesinuse** vom Windows Installer ignoriert.

-   Eine Windows Installer Version, die nicht älter als Version 4,0 ist, und ein Betriebssystem, das nicht älter als Windows Vista oder Windows Server 2008 ist, führt die Installation aus.
-   Die [Benutzeroberflächen Ebene](user-interface-levels.md) "vollständig" wird verwendet.
-   Interaktionen mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) wurden nicht durch die [**msirestartmanagercontrol**](msirestartmanagercontrol.md) -Eigenschaft oder die [disableautomaticapplicationshutdown](disableautomaticapplicationshutdown.md) -Richtlinie deaktiviert.
-   Das Dialogfeld **msirmfilesinuse** ist im Installationspaket enthalten.
-   Alle Aufrufe des Windows Installer an den [Neustart-Manager](../rstmgr/restart-manager-portal.md) sind erfolgreich.

Dieses Dialogfeld wird entsprechend der [InstallValidate-Aktion](installvalidate-action.md)erstellt.

 

 
