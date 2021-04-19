---
description: Unter den Betriebssystemen Windows XP und höher legt das Installationsprogramm die Eigenschaft msintsuitepersonal auf 1 fest, wenn das Betriebssystem Windows XP Home Edition ist.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Msintsuitepersonal (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369658"
---
# <a name="msintsuitepersonal-property"></a><span data-ttu-id="a530c-103">Msintsuitepersonal (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a530c-103">MsiNTSuitePersonal property</span></span>

<span data-ttu-id="a530c-104">Unter den Betriebssystemen Windows XP und höher legt das Installationsprogramm die Eigenschaft **msintsuitepersonal** auf 1 fest, wenn das Betriebssystem Windows XP Home Edition ist.</span><span class="sxs-lookup"><span data-stu-id="a530c-104">On Windows XP and later operating systems, the installer sets the **MsiNTSuitePersonal** property to 1 if the operating system is Windows XP Home Edition.</span></span> <span data-ttu-id="a530c-105">Der Installer legt diese Eigenschaft nur dann auf 1 fest, wenn das \_ kennflag der Ver Suite \_ in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a530c-105">The installer sets this property to 1 only if the VER\_SUITE\_PERSONAL flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="a530c-106">Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.</span><span class="sxs-lookup"><span data-stu-id="a530c-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a530c-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a530c-107">Requirements</span></span>



| <span data-ttu-id="a530c-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a530c-108">Requirement</span></span> | <span data-ttu-id="a530c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="a530c-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a530c-110">Version</span><span class="sxs-lookup"><span data-stu-id="a530c-110">Version</span></span><br/> | <span data-ttu-id="a530c-111">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a530c-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a530c-112">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a530c-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a530c-113">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a530c-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a530c-114">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a530c-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a530c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a530c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a530c-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a530c-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
