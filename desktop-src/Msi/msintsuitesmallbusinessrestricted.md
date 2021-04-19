---
description: Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die Eigenschaft msintsuitesmallbusinessrestricted auf 1 fest, wenn Microsoft Small Business Server mit der eingeschränkten Client Lizenz in Kraft installiert wird.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Msintsuitesmallbusinessrestricted (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369492"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a><span data-ttu-id="b2228-103">Msintsuitesmallbusinessrestricted (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b2228-103">MsiNTSuiteSmallBusinessRestricted property</span></span>

<span data-ttu-id="b2228-104">Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die Eigenschaft **msintsuitesmallbusinessrestricted** auf 1 fest, wenn Microsoft Small Business Server mit der eingeschränkten Client Lizenz in Kraft installiert wird.</span><span class="sxs-lookup"><span data-stu-id="b2228-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusinessRestricted** property to 1 if Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="b2228-105">Der Installer legt diese Eigenschaft nur dann auf 1 fest, wenn das Flag der Ver \_ Suite \_ SmallBusiness \_ restricted in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b2228-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS\_RESTRICTED flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="b2228-106">Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.</span><span class="sxs-lookup"><span data-stu-id="b2228-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2228-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2228-107">Requirements</span></span>



| <span data-ttu-id="b2228-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2228-108">Requirement</span></span> | <span data-ttu-id="b2228-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b2228-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2228-110">Version</span><span class="sxs-lookup"><span data-stu-id="b2228-110">Version</span></span><br/> | <span data-ttu-id="b2228-111">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b2228-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b2228-112">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2228-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b2228-113">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2228-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b2228-114">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b2228-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2228-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2228-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2228-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2228-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
