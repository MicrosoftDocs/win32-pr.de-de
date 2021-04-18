---
description: Benachrichtigt den Windows Installer, mit dem Neustart-Manager alle Anwendungen mit verwendeten Dateien herunterzufahren und am Ende der Installation neu zu starten.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: Rmshutdownandrestart ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343774"
---
# <a name="rmshutdownandrestart-controlevent"></a><span data-ttu-id="57a58-103">Rmshutdownandrestart ControlEvent</span><span class="sxs-lookup"><span data-stu-id="57a58-103">RmShutdownAndRestart ControlEvent</span></span>

<span data-ttu-id="57a58-104">Dieses Ereignis benachrichtigt den Windows Installer, den Neustart- [Manager](../rstmgr/restart-manager-portal.md) zu verwenden, um alle Anwendungen mit verwendeten Dateien herunterzufahren und am Ende der Installation neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="57a58-104">This event notifies the Windows Installer to use the [Restart Manager](../rstmgr/restart-manager-portal.md) to shutdown all applications that have files in use and to restart them at the end of the installation.</span></span>

<span data-ttu-id="57a58-105">Dieses ControlEvent hat keine Auswirkung, wenn eine der folgenden Punkte zutrifft.</span><span class="sxs-lookup"><span data-stu-id="57a58-105">This ControlEvent has no effect if any of the following are true.</span></span>

-   <span data-ttu-id="57a58-106">Das Betriebssystem, auf dem die Installation ausgeführt wird, ist nicht Windows Vista oder Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="57a58-106">The operating system running the installation is not Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="57a58-107">Interaktionen mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) wurden durch die [**msirestartmanagercontrol**](msirestartmanagercontrol.md) -Eigenschaft oder die [disableautomaticapplicationshutdown](disableautomaticapplicationshutdown.md) -Richtlinie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="57a58-107">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="57a58-108">Zurzeit ist keine geöffnete [Neustart-Manager](../rstmgr/restart-manager-portal.md) -Sitzung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="57a58-108">There is currently no open [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>
-   <span data-ttu-id="57a58-109">Bei allen Aufrufen der Windows Installer an den [Neustart-Manager](../rstmgr/restart-manager-portal.md) wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="57a58-109">Any calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) returns a failure.</span></span>

## <a name="typical-use"></a><span data-ttu-id="57a58-110">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="57a58-110">Typical Use</span></span>

<span data-ttu-id="57a58-111">Das Ereignis rmshutdownandrestart-Steuerelement wird nur von einem [PUSHBUTTON](pushbutton-control.md) -Steuerelement im [Dialog Feld msirmfilesinuse](msirmfilesinuse-dialog.md) veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="57a58-111">The RMShutdownAndRestart control event is published only by a [PushButton](pushbutton-control.md) control on the [MsiRMFilesInUse Dialog](msirmfilesinuse-dialog.md) box.</span></span>

 

 
