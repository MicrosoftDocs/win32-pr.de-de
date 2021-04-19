---
description: Bei der Systemwiederherstellung werden wichtige Systemänderungen auf dem Computer eines Benutzers automatisch überwacht und aufgezeichnet. Weitere Informationen finden Sie unter System Wiederherstellung.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: System Wiederherstellungspunkte und die Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359914"
---
# <a name="system-restore-points-and-the-windows-installer"></a><span data-ttu-id="7562c-104">System Wiederherstellungspunkte und die Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7562c-104">System Restore Points and the Windows Installer</span></span>

<span data-ttu-id="7562c-105">Bei der Systemwiederherstellung werden wichtige Systemänderungen auf dem Computer eines Benutzers automatisch überwacht und aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7562c-105">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="7562c-106">Weitere Informationen finden Sie unter [System Wiederherstellung](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="7562c-106">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="7562c-107">System Wiederherstellungspunkte werden vom System erstellt und auch Windows Installer erstellt, wenn Software installiert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7562c-107">System restore points are created by the system and are also created by Windows Installer when software is installed or removed.</span></span>

<span data-ttu-id="7562c-108">Unter Windows XP kann das Installationsprogramm während der ersten Installation einer Anwendung und während des Entfernens Prüfpunkte erstellen.</span><span class="sxs-lookup"><span data-stu-id="7562c-108">On Windows XP, the installer may create checkpoints during the first installation of an application, and during its removal.</span></span> <span data-ttu-id="7562c-109">Der Installer erstellt in diesen Fällen nur Prüfpunkte, wenn die Änderung mit mindestens einer [*grundlegenden Benutzeroberfläche*](b-gly.md)ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7562c-109">The installer only creates checkpoints in these cases when the change is run with at least a [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="7562c-110">Installationen, bei denen die [Benutzeroberflächen Ebene](user-interface-levels.md) auf None festgelegt ist, werden normalerweise vom System oder einer Anwendung initiiert, die das Erstellen eines Prüf Punkts behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="7562c-110">Installations having the [user interface level](user-interface-levels.md) set to None are usually initiated by the system or an application that should handle creating a checkpoint.</span></span> <span data-ttu-id="7562c-111">Weitere Informationen finden Sie unter [System Wiederherstellung](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="7562c-111">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="7562c-112">In Unternehmen mit vielen kleinen Anwendungen können Administratoren festlegen, dass die Prüfpunkte im Installer deaktiviert werden, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7562c-112">In corporations with many small applications, administrators may decide to disable checkpointing from within the installer to improve performance.</span></span> <span data-ttu-id="7562c-113">Weitere Informationen finden Sie unter [limitsystemrestorecheckpointpunkt](limitsystemrestorecheckpointing.md) oder [Festlegen eines Wiederherstellungs Punkts aus einer benutzerdefinierten Aktion](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="7562c-113">For more information, see [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) or [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

<span data-ttu-id="7562c-114">Ab Windows Installer 5,0 kann die [**msifastinstall**](msifastinstall.md) -Eigenschaft festgelegt werden, um zu verhindern, dass eine Installation einen Systemwiederherstellungspunkt erzeugt.</span><span class="sxs-lookup"><span data-stu-id="7562c-114">Beginning with Windows Installer 5.0, the [**MSIFASTINSTALL**](msifastinstall.md) property can be set to prevent an installation from generating a system restore point.</span></span>

 

 
