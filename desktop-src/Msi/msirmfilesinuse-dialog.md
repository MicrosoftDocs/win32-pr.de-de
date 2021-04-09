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
# <a name="msirmfilesinuse-dialog"></a><span data-ttu-id="6a578-103">Dialog Feld "msirmfilesinuse"</span><span class="sxs-lookup"><span data-stu-id="6a578-103">MsiRMFilesInUse Dialog</span></span>

<span data-ttu-id="6a578-104">Das Dialog Feld msirmfilesinuse kann erstellt werden, um eine Liste der Prozesse anzuzeigen, die derzeit Dateien ausführen, die bei der Installation überschrieben oder gelöscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6a578-104">The MsiRMFilesInUse Dialog box can be authored to display a list of processes that are currently running files that need to be overwritten or deleted by the installation.</span></span> <span data-ttu-id="6a578-105">Der Benutzer kann zwischen Optionen zum automatischen Schließen von Anwendungen und Neustarten oder "Anwendungen nicht schließen" auswählen.</span><span class="sxs-lookup"><span data-stu-id="6a578-105">The user can select between options to "Automatically close applications and restart them" or "Do not close applications.</span></span> <span data-ttu-id="6a578-106">(Ein Neustart ist erforderlich.) Wenn der Benutzer die Option "Anwendungen automatisch schließen und neu starten" auswählt, kann ein Push-Schaltflächen-Steuerelement in diesem Dialogfeld erstellt werden, um das rmshutdownandrestart-Steuerungs Ereignis zu veröffentlichen, und der [Neustart-Manager](../rstmgr/restart-manager-portal.md) kann die Anwendungen schließen und am Ende der Installation neu starten.</span><span class="sxs-lookup"><span data-stu-id="6a578-106">(A reboot will be required.)" If the user selects the "Automatically close applications and restart them" option, a push button control on this dialog box can be authored to publish the RMShutdownAndRestart control event and the [Restart Manager](../rstmgr/restart-manager-portal.md) can close the applications and restart them at the end of the installation.</span></span> <span data-ttu-id="6a578-107">Dadurch kann der Computer nicht neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6a578-107">This can eliminate or reduce the need to restart the computer.</span></span> <span data-ttu-id="6a578-108">Weitere Informationen finden Sie unter [System Neustarts](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="6a578-108">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="6a578-109">Das Dialogfeld **msirmfilesinuse** wird nur während einer Installation angezeigt, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6a578-109">The **MsiRMFilesInUse** dialog box is displayed during an installation only if all the following are true.</span></span> <span data-ttu-id="6a578-110">Wenn eine dieser beiden Typen false ist, wird das Dialogfeld **msirmfilesinuse** vom Windows Installer ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6a578-110">When any of these are false, the Windows Installer ignores the **MsiRMFilesInUse** dialog box.</span></span>

-   <span data-ttu-id="6a578-111">Eine Windows Installer Version, die nicht älter als Version 4,0 ist, und ein Betriebssystem, das nicht älter als Windows Vista oder Windows Server 2008 ist, führt die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="6a578-111">A Windows Installer version that is not earlier than version 4.0 and an operating system that is not earlier than Windows Vista or Windows Server 2008 is running the installation.</span></span>
-   <span data-ttu-id="6a578-112">Die [Benutzeroberflächen Ebene](user-interface-levels.md) "vollständig" wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a578-112">The Full UI [user interface level](user-interface-levels.md) is used.</span></span>
-   <span data-ttu-id="6a578-113">Interaktionen mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) wurden nicht durch die [**msirestartmanagercontrol**](msirestartmanagercontrol.md) -Eigenschaft oder die [disableautomaticapplicationshutdown](disableautomaticapplicationshutdown.md) -Richtlinie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6a578-113">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have not been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="6a578-114">Das Dialogfeld **msirmfilesinuse** ist im Installationspaket enthalten.</span><span class="sxs-lookup"><span data-stu-id="6a578-114">The **MsiRMFilesInUse** dialog box is present in the installation package.</span></span>
-   <span data-ttu-id="6a578-115">Alle Aufrufe des Windows Installer an den [Neustart-Manager](../rstmgr/restart-manager-portal.md) sind erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6a578-115">All calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) are successful.</span></span>

<span data-ttu-id="6a578-116">Dieses Dialogfeld wird entsprechend der [InstallValidate-Aktion](installvalidate-action.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="6a578-116">This dialog box will be created as required by the [InstallValidate action](installvalidate-action.md).</span></span>

 

 
