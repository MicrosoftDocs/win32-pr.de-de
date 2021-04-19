---
description: Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die Eigenschaft msintsuitewebserver auf 1 fest, wenn das Installationsprogramm auf einer Web Edition von Windows Server 2003 ausgeführt wird.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Msintsuitewebserver (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370655"
---
# <a name="msintsuitewebserver-property"></a><span data-ttu-id="27061-103">Msintsuitewebserver (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="27061-103">MsiNTSuiteWebServer property</span></span>

<span data-ttu-id="27061-104">Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die Eigenschaft **msintsuitewebserver** auf 1 fest, wenn das Installationsprogramm auf einer Web Edition von Windows Server 2003 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27061-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteWebServer** property to 1 if the installer is running on a web edition of the Windows Server 2003.</span></span> <span data-ttu-id="27061-105">Der Installer legt diese Eigenschaft nur dann auf 1 fest, wenn das Blatt "Ver \_ Suite \_ Blade" in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="27061-105">The installer sets this property to 1 only if the VER\_SUITE\_BLADE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="27061-106">Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.</span><span class="sxs-lookup"><span data-stu-id="27061-106">Otherwise the installer does not set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="27061-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27061-107">Remarks</span></span>

<span data-ttu-id="27061-108">Diese Eigenschaft ist nur mit der Windows Server 2003-Version des Installationsprogramms verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27061-108">This property is available only with the Windows Server 2003 release of the installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="27061-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27061-109">Requirements</span></span>



| <span data-ttu-id="27061-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27061-110">Requirement</span></span> | <span data-ttu-id="27061-111">Wert</span><span class="sxs-lookup"><span data-stu-id="27061-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27061-112">Version</span><span class="sxs-lookup"><span data-stu-id="27061-112">Version</span></span><br/> | <span data-ttu-id="27061-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="27061-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="27061-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="27061-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="27061-115">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27061-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="27061-116">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="27061-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27061-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27061-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27061-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27061-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="27061-119">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27061-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
