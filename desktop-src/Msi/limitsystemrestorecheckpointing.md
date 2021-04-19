---
description: Diese pro-Computer-System Richtlinie deaktiviert die Erstellung von Prüfpunkten durch Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: Limitsystemrestorecheckpoints
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348407"
---
# <a name="limitsystemrestorecheckpointing"></a><span data-ttu-id="7d1c0-103">Limitsystemrestorecheckpoints</span><span class="sxs-lookup"><span data-stu-id="7d1c0-103">LimitSystemRestoreCheckpointing</span></span>

<span data-ttu-id="7d1c0-104">Diese pro-Computer- [System Richtlinie](system-policy.md) deaktiviert die Erstellung von Prüfpunkten durch Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7d1c0-104">This per-machine [system policy](system-policy.md) turns off the creation of checkpoints by Windows Installer.</span></span>

<span data-ttu-id="7d1c0-105">Wenn der Wert 0 (null) oder nicht vorhanden ist, führt der Installer für die Installation oder Deinstallation eine normale</span><span class="sxs-lookup"><span data-stu-id="7d1c0-105">Set to 0 or absent, the installer does normal checkpointing for install or uninstall.</span></span> <span data-ttu-id="7d1c0-106">Auf 1 festgelegt ist, erstellt das Installationsprogramm keine Prüfpunkte.</span><span class="sxs-lookup"><span data-stu-id="7d1c0-106">Set to 1, the installer creates no checkpoints.</span></span>

<span data-ttu-id="7d1c0-107">Diese Richtlinie wirkt sich nur auf Prüfpunkte aus, die von Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7d1c0-107">This policy affects only checkpoints set by Windows Installer.</span></span> <span data-ttu-id="7d1c0-108">Auf Windows XP-Computern können Administratoren festlegen, dass Prüfpunkte in Windows Installer deaktiviert werden, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7d1c0-108">On Windows XP computers, administrators may decide to disable checkpointing from within Windows Installer to improve performance.</span></span> <span data-ttu-id="7d1c0-109">Die [**System Wiederherstellung**](../sr/system-restore-portal.md) erstellt auch zusätzliche Prüfpunkte.</span><span class="sxs-lookup"><span data-stu-id="7d1c0-109">[**System Restore**](../sr/system-restore-portal.md) also creates additional checkpoints.</span></span> <span data-ttu-id="7d1c0-110">Weitere Informationen finden Sie unter [System Wiederherstellungspunkte und die Windows Installer](system-restore-points-and-the-windows-installer.md) und [Festlegen eines Wiederherstellungs Punkts aus einer benutzerdefinierten Aktion](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="7d1c0-110">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md) and [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="7d1c0-111">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="7d1c0-111">Registry Key</span></span>

<span data-ttu-id="7d1c0-112">Legen Sie den Wert limitsystemrestorecheckpoints unter dem folgenden Registrierungsschlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="7d1c0-112">Set the value named LimitSystemRestoreCheckpointing under the following registry key.</span></span>

<span data-ttu-id="7d1c0-113">**\_Software Richtlinien für den lokalen HKEY- \_ Computer \\ \\ \\ Microsoft \\ Windows \\ Installer**</span><span class="sxs-lookup"><span data-stu-id="7d1c0-113">**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="7d1c0-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7d1c0-114">Data Type</span></span>

<span data-ttu-id="7d1c0-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7d1c0-115">**REG\_DWORD**</span></span>

 

 
