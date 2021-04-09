---
description: Wenn diese Computer spezifische System Richtlinie nicht festgelegt ist, können nur Administratoren vorhandene Produkte Patchen, die mit erhöhten Rechten installiert wurden.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: Allowlockdownpatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959540"
---
# <a name="allowlockdownpatch"></a><span data-ttu-id="a0e1a-103">Allowlockdownpatch</span><span class="sxs-lookup"><span data-stu-id="a0e1a-103">AllowLockdownPatch</span></span>

<span data-ttu-id="a0e1a-104">Wenn diese Computer spezifische [System Richtlinie](system-policy.md) nicht festgelegt ist, können nur Administratoren vorhandene Produkte Patchen, die mit erhöhten Rechten installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-104">If this per-machine [system policy](system-policy.md) is not set, only administrators can patch existing products that were installed using elevated privileges.</span></span> <span data-ttu-id="a0e1a-105">Wenn allowlockdownpatch auf "1" festgelegt ist, können Benutzer, die nicht Administratoren sind, in einigen Fällen Patches auf Produkte anwenden, während eine Installation mit erhöhten Rechten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-105">If AllowLockdownPatch is set to "1", nonadministrative users can, in some cases, apply patches to products while running an installation using elevated privileges.</span></span> <span data-ttu-id="a0e1a-106">Wenn die Richtlinie festgelegt ist, kann der Patch [kleinere Upgrades](minor-upgrades.md) installieren, während eine Installation mit erhöhten Rechten ausgeführt wird. der Patch kann keine [größeren Upgrades](major-upgrades.md)installieren.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-106">With the policy set, the patch can install [minor upgrades](minor-upgrades.md) while running an installation using elevated privileges, the patch cannot install [major upgrades](major-upgrades.md).</span></span> <span data-ttu-id="a0e1a-107">Wenn Sie diese Richtlinie festlegen, können Benutzer, die nicht Administratoren sind, auch bei einer erweiterten Installation Programme mit LocalSystem-Berechtigungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="a0e1a-108">Die Standardeinstellung wird empfohlen, um eine sichere Umgebung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-108">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="a0e1a-109">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="a0e1a-109">Registry Key</span></span>

<span data-ttu-id="a0e1a-110">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="a0e1a-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a0e1a-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a0e1a-111">Data Type</span></span>

<span data-ttu-id="a0e1a-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a0e1a-112">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="a0e1a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0e1a-113">Remarks</span></span>

<span data-ttu-id="a0e1a-114">Jeder Benutzer kann einen Patch während einer Installation ohne erhöhte Rechte anwenden.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-114">Any user can apply a patch during a nonelevated installation.</span></span> <span data-ttu-id="a0e1a-115">Wenn Sie diese pro-Computer- [System Richtlinie](system-policy.md) auf "1" festlegen, erhalten nicht Administratoren zusätzliche Flexibilität bei der Anwendung von Patches auf beliebige Produkte.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-115">Setting this per-machine [system policy](system-policy.md) to "1" gives nonadministrative users the additional flexibility of applying patches to any product during an elevated installation.</span></span> <span data-ttu-id="a0e1a-116">Wenn diese Richtlinie nicht festgelegt ist, können nicht-Administratoren einen Patch auf zugewiesene oder veröffentlichte Anwendungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-116">If this policy is not set, nonadministrative users cannot apply a patch to assigned or published applications.</span></span>

<span data-ttu-id="a0e1a-117">Durch Festlegen dieser Richtlinie können nicht Administratoren beliebige Programme unter "LocalSystem"-Privilegien ausführen, wenn Sie über ein Windows Installer Patch-Paket verfügen, das diese Programme installiert oder gestartet.</span><span class="sxs-lookup"><span data-stu-id="a0e1a-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer patch package that installs or launches those programs.</span></span>

 

 



