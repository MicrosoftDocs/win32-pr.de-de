---
description: Wenn diese pro-Computer-System Richtlinie auf 1 (eins) festgelegt ist, wird Windows Installer nicht mit dem Neustart-Manager interagieren, aber das Dialogfeld FilesInUse verwendet. wenn diese pro-Computer-System Richtlinie auf 2 (2) festgelegt ist, verwendet Windows Installer das FilesInUse-Dialogfeld.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: Disableautomaticapplicationshutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356898"
---
# <a name="disableautomaticapplicationshutdown"></a><span data-ttu-id="0e8b1-103">Disableautomaticapplicationshutdown</span><span class="sxs-lookup"><span data-stu-id="0e8b1-103">DisableAutomaticApplicationShutdown</span></span>

<span data-ttu-id="0e8b1-104">Wenn diese Computer spezifische System Richtlinie auf 1 (eins) festgelegt ist, interagiert Windows Installer nicht mit dem [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal), sondern verwendet das [Dialog Feld FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="0e8b1-104">If this per-machine system policy is set to 1 (one), Windows Installer does not interact with [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal), but it will use the [FilesInUse Dialog](filesinuse-dialog.md).</span></span>

<span data-ttu-id="0e8b1-105">Wenn diese pro-Computer-System Richtlinie auf 2 (2) festgelegt ist, wird Windows Installer das [FilesInUse-Dialog](filesinuse-dialog.md)Feld verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-105">If this per-machine system policy is set to 2 (two), Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="0e8b1-106">Mit dieser Einstellung werden Versuche durch den [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal) deaktiviert, um beim Installieren eines Windows Installer Pakets, das noch nicht für die Verwendung des Neustart-Managers erstellt wurde, Neustarts zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-106">This setting disables attempts by the [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="0e8b1-107">Der Installer verwendet weiterhin den Neustart-Manager, um die von Anwendungen verwendeten Dateien zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-107">The installer still uses the Restart Manager to detect files in use by applications.</span></span>

<span data-ttu-id="0e8b1-108">Die disableautomaticapplicationshutdown-Richtlinie ist ab Windows Installer Version 4,0 unter Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-108">The DisableAutomaticApplicationShutdown policy is available beginning with Windows Installer version 4.0 on Windows Vista.</span></span>

## <a name="registry-key"></a><span data-ttu-id="0e8b1-109">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="0e8b1-109">Registry Key</span></span>

<span data-ttu-id="0e8b1-110">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="0e8b1-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="0e8b1-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0e8b1-111">Data Type</span></span>

<span data-ttu-id="0e8b1-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0e8b1-112">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e8b1-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e8b1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e8b1-114">**MSIRESTARTMANAGERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="0e8b1-114">**MSIRESTARTMANAGERCONTROL**</span></span>](msirestartmanagercontrol.md)
</dt> <dt>

[<span data-ttu-id="0e8b1-115">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-115">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
