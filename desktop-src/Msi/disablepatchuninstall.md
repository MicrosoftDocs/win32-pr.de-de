---
description: Wenn diese pro-Computer-System Richtlinie auf 1 festgelegt ist, können Patches von einem Benutzer oder Administrator nicht vom Computer entfernt werden.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: Disablepatchuninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863043"
---
# <a name="disablepatchuninstall"></a><span data-ttu-id="91d0c-103">Disablepatchuninstall</span><span class="sxs-lookup"><span data-stu-id="91d0c-103">DisablePatchUninstall</span></span>

<span data-ttu-id="91d0c-104">Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf 1 festgelegt ist, können Patches von einem Benutzer oder Administrator nicht vom Computer entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="91d0c-104">If this per-machine [system policy](system-policy.md) is set to 1, patches cannot be removed from the computer by a user or an administrator.</span></span> <span data-ttu-id="91d0c-105">Der Windows Installer kann weiterhin einen Patch entfernen, der für ein Produkt nicht mehr anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="91d0c-105">The Windows Installer can still remove a patch that is no longer applicable to a product.</span></span> <span data-ttu-id="91d0c-106">Wenn diese Richtlinie nicht festgelegt ist, kann ein Benutzer einen Patch nur dann vom Computer entfernen, wenn dem Benutzerberechtigungen zum Entfernen des Patches erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="91d0c-106">If this policy is not set, a user can remove a patch from the computer only if the user has been granted privileges to remove the patch.</span></span> <span data-ttu-id="91d0c-107">Dies kann davon abhängen, ob der Benutzer ein Administrator ist, ob die Richtlinien Einstellungen [DisableMSI](disablemsi.md) und [alwaysinstallerhöhten](alwaysinstallelevated.md) festgelegt sind und ob der Patch in einem pro Benutzer verwalteten, nicht verwalteten oder benutzerspezifischen Kontext installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="91d0c-107">This can depend on whether the user is an administrator, whether [DisableMsi](disablemsi.md) and [AlwaysInstallElevated](alwaysinstallelevated.md) policy settings are set, and whether the patch was installed in a per-user managed, per-user unmanaged, or per-machine context.</span></span>

## <a name="registry-key"></a><span data-ttu-id="91d0c-108">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="91d0c-108">Registry Key</span></span>

<span data-ttu-id="91d0c-109">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="91d0c-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="91d0c-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="91d0c-110">Data Type</span></span>

<span data-ttu-id="91d0c-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="91d0c-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="91d0c-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91d0c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91d0c-113">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91d0c-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



