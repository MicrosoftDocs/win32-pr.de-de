---
description: Ab Windows Server 2008 und Windows Vista hat diese Richtlinie keine Auswirkungen mehr.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: Enableadminout-Remote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215128"
---
# <a name="enableadmintsremote"></a><span data-ttu-id="5d126-103">Enableadminout-Remote</span><span class="sxs-lookup"><span data-stu-id="5d126-103">EnableAdminTSRemote</span></span>

<span data-ttu-id="5d126-104">Ab Windows Server 2008 und Windows Vista hat diese Richtlinie keine Auswirkungen mehr.</span><span class="sxs-lookup"><span data-stu-id="5d126-104">Beginning with Windows Server 2008 and Windows Vista, this policy no longer has any effect.</span></span> <span data-ttu-id="5d126-105">Ein Administrator kann eine Installation über die Konsolen Sitzung eines Terminal Servers ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d126-105">An administrator can perform an installation from the console session of a terminal server.</span></span> <span data-ttu-id="5d126-106">Ein Administrator kann auch eine Installation aus einer Client Sitzung des Terminal Servers ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d126-106">An administrator can also perform an installation from a client session of the terminal server.</span></span>

<span data-ttu-id="5d126-107">Weitere Informationen finden Sie unter [Terminal Dienste](/windows/desktop/TermServ/terminal-services-portal) im Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5d126-107">For more information, see [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) in the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="5d126-108">\* \* Betriebssysteme vor Windows Server 2008 und Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="5d126-108">\*\*Operating systems earlier than Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="5d126-109">Durch Festlegen dieser computerspezifischen [System Richtlinie](system-policy.md) können Administratoren Installationen aus einer Client Sitzung des Terminal Servers ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d126-109">Setting this per-machine [system policy](system-policy.md) enables administrators to perform installations from a client session of the terminal server.</span></span> <span data-ttu-id="5d126-110">Wenn diese Richtlinie nicht festgelegt ist, können Administratoren nur Installationen aus der Konsolen Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d126-110">If this policy is not set, administrators can only perform installations from the console session.</span></span> <span data-ttu-id="5d126-111">Nicht Administratoren können niemals Installationen aus einer Client Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d126-111">Nonadministrative users can never perform installations from a client session.</span></span> <span data-ttu-id="5d126-112">Der Standardwert für diese Richtlinie ermöglicht es nur Administratoren, Installationen über die Konsolen Sitzung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5d126-112">The default value for this policy allows only administrators to perform installations from the console session.</span></span> <span data-ttu-id="5d126-113">Administratoren können immer [administrative Installationen](administrative-installation.md) über eine Client Sitzung des Terminal Servers oder über die Konsolen Sitzung ausführen, unabhängig davon, ob diese Richtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5d126-113">Administrators can always do [Administrative installations](administrative-installation.md) from a client session of the terminal server, or from the console session, regardless of whether this policy is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="5d126-114">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="5d126-114">Registry Key</span></span>

<span data-ttu-id="5d126-115">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="5d126-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="5d126-116">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5d126-116">Data Type</span></span>

<span data-ttu-id="5d126-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5d126-117">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="5d126-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d126-118">Remarks</span></span>

<span data-ttu-id="5d126-119">Weitere Informationen finden [Sie unter Verwenden von Windows Installer mit einem Terminal Server](using-windows-installer-with-a-terminal-server.md).</span><span class="sxs-lookup"><span data-stu-id="5d126-119">For more information see also, [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).</span></span>

 

 
