---
description: Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die msintsuitedatacenter-Eigenschaft auf 1 fest, wenn Windows 2000 Datacenter Server installiert ist.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: Msintsuitedatacenter (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106b9119885e15b94bf5d8f2cd4b6954d0891d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362114"
---
# <a name="msintsuitedatacenter-property"></a><span data-ttu-id="307b4-103">Msintsuitedatacenter (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="307b4-103">MsiNTSuiteDataCenter property</span></span>

<span data-ttu-id="307b4-104">Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die **msintsuitedatacenter** -Eigenschaft auf 1 fest, wenn Windows 2000 Datacenter Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="307b4-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteDataCenter** property to 1 if Windows 2000 Datacenter Server is installed.</span></span> <span data-ttu-id="307b4-105">Der Installer legt diese Eigenschaft nur dann auf 1 fest, wenn das Ver \_ Suite \_ Datacenter-Flag in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="307b4-105">The installer sets this property to 1 only if the VER\_SUITE\_DATACENTER flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="307b4-106">Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.</span><span class="sxs-lookup"><span data-stu-id="307b4-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="307b4-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="307b4-107">Requirements</span></span>



| <span data-ttu-id="307b4-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="307b4-108">Requirement</span></span> | <span data-ttu-id="307b4-109">Wert</span><span class="sxs-lookup"><span data-stu-id="307b4-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b4-110">Version</span><span class="sxs-lookup"><span data-stu-id="307b4-110">Version</span></span><br/> | <span data-ttu-id="307b4-111">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="307b4-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="307b4-112">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="307b4-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="307b4-113">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="307b4-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="307b4-114">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="307b4-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="307b4-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="307b4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="307b4-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="307b4-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
