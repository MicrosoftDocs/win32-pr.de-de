---
description: Das Installationsprogramm legt die VersionNT-Eigenschaft auf die Versionsnummer des Betriebssystems fest. Dies ist nicht definiert, wenn das Betriebssystem nicht Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 oder Windows 7 entspricht.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: VersionNT-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358115"
---
# <a name="versionnt-property"></a><span data-ttu-id="eab5e-103">VersionNT-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eab5e-103">VersionNT property</span></span>

<span data-ttu-id="eab5e-104">Das Installationsprogramm legt die **VersionNT** -Eigenschaft auf die Versionsnummer des Betriebssystems fest. Dies ist nicht definiert, wenn das Betriebssystem nicht Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 oder Windows 7 entspricht.</span><span class="sxs-lookup"><span data-stu-id="eab5e-104">The installer sets the **VersionNT** property to the version number for the operating system, undefined if the operating system is not Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008, or Windows 7.</span></span> <span data-ttu-id="eab5e-105">Der Wert ist eine ganze Zahl: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="eab5e-105">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="eab5e-106">Bedingte Anweisungen, die vom Betriebssystem abhängen, können diese Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="eab5e-106">Conditional statements that depend upon the operating system can use this property.</span></span>

<span data-ttu-id="eab5e-107">Siehe auch [Betriebs System-Eigenschaftswerte](operating-system-property-values.md).</span><span class="sxs-lookup"><span data-stu-id="eab5e-107">See also [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eab5e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eab5e-108">Remarks</span></span>

<span data-ttu-id="eab5e-109">Bedingungs Ausdrücke können mit dem Eigenschaftsnamen auf Windows NT, Windows 2000 oder Windows XP testen oder die Version mithilfe eines Vergleichs Operators überprüfen.</span><span class="sxs-lookup"><span data-stu-id="eab5e-109">Condition expressions can test for Windows NT, Windows 2000, or Windows XP by using the property name, or may verify the version by using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab5e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eab5e-110">Requirements</span></span>



| <span data-ttu-id="eab5e-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eab5e-111">Requirement</span></span> | <span data-ttu-id="eab5e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="eab5e-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab5e-113">Version</span><span class="sxs-lookup"><span data-stu-id="eab5e-113">Version</span></span><br/> | <span data-ttu-id="eab5e-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eab5e-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eab5e-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eab5e-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eab5e-116">Windows Installer unter Windows Server 2003 oder Windows XP finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eab5e-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eab5e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eab5e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab5e-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eab5e-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




