---
description: Der Installer legt die msitabletpc-Eigenschaft auf einen Wert ungleich 0 (null) fest, wenn das aktuelle Betriebssystem Windows XP Tablet PC Edition ist.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Msitabletpc (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362042"
---
# <a name="msitabletpc-property"></a><span data-ttu-id="21d4d-103">Msitabletpc (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="21d4d-103">MsiTabletPC property</span></span>

<span data-ttu-id="21d4d-104">Der Installer legt die **msitabletpc** -Eigenschaft auf einen Wert ungleich 0 (null) fest, wenn das aktuelle Betriebssystem Windows XP Tablet PC Edition ist.</span><span class="sxs-lookup"><span data-stu-id="21d4d-104">The installer sets the **MsiTabletPC** property to a nonzero value if the current operating system is Windows XP Tablet PC Edition.</span></span> <span data-ttu-id="21d4d-105">Das Installationsprogramm verwendet die [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion mit **SM \_ TabletPC**, und die-Eigenschaft empfängt den von dieser Funktion zurückgegebenen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="21d4d-105">The installer uses the [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function with **SM\_TABLETPC**, and the property receives the nonzero value returned by this function.</span></span> <span data-ttu-id="21d4d-106">Wenn das aktuelle System nicht Windows XP Tablet PC Edition ist, gibt die **GetSystemMetrics** -Funktion 0 (null) zurück, und das Installationsprogramm legt diese Eigenschaft nicht fest.</span><span class="sxs-lookup"><span data-stu-id="21d4d-106">If the current system is not Windows XP Tablet PC Edition, the **GetSystemMetrics** function returns zero and the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d4d-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21d4d-107">Requirements</span></span>



| <span data-ttu-id="21d4d-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21d4d-108">Requirement</span></span> | <span data-ttu-id="21d4d-109">Wert</span><span class="sxs-lookup"><span data-stu-id="21d4d-109">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21d4d-110">Version</span><span class="sxs-lookup"><span data-stu-id="21d4d-110">Version</span></span><br/> | <span data-ttu-id="21d4d-111">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="21d4d-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="21d4d-112">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="21d4d-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="21d4d-113">Windows Installer 4,5 unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21d4d-113">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="21d4d-114">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="21d4d-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21d4d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21d4d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d4d-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21d4d-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="21d4d-117">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21d4d-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
