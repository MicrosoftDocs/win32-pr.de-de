---
description: Der Installer legt die VersionNT64-Eigenschaft nur dann auf die Versionsnummer des Betriebssystems fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352933"
---
# <a name="versionnt64-property"></a><span data-ttu-id="375f8-103">VersionNT64-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="375f8-103">VersionNT64 property</span></span>

<span data-ttu-id="375f8-104">Der Installer legt die **VersionNT64** -Eigenschaft nur dann auf die Versionsnummer des Betriebssystems fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="375f8-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="375f8-105">Die-Eigenschaft ist nicht definiert, wenn das Betriebssystem nicht 64-Bit ist.</span><span class="sxs-lookup"><span data-stu-id="375f8-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="375f8-106">Der Wert ist eine ganze Zahl: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="375f8-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="375f8-107">Aus Kompatibilitätsgründen wird die-Eigenschaft ebenfalls nicht definiert, wenn die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft angibt, dass das Paket für 32-Bit-Intel-Systeme und das Betriebssystem eine 64-Bit-Architektur ist, die nicht Intel64 oder x64 ist (z. b. ARM64).</span><span class="sxs-lookup"><span data-stu-id="375f8-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel systems and the operating system is a 64-bit architecture that is not Intel64 or x64 (such as ARM64).</span></span>

## <a name="remarks"></a><span data-ttu-id="375f8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="375f8-108">Remarks</span></span>

<span data-ttu-id="375f8-109">Bedingte Ausdrücke testen für 64-Bit-Fenster einfach mithilfe des Eigenschafts namens oder durch Überprüfen der Version mithilfe eines Vergleichs Operators.</span><span class="sxs-lookup"><span data-stu-id="375f8-109">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="375f8-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="375f8-110">Requirements</span></span>



| <span data-ttu-id="375f8-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="375f8-111">Requirement</span></span> | <span data-ttu-id="375f8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="375f8-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="375f8-113">Version</span><span class="sxs-lookup"><span data-stu-id="375f8-113">Version</span></span><br/> | <span data-ttu-id="375f8-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="375f8-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="375f8-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="375f8-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="375f8-116">Windows Installer unter Windows Server 2003 oder Windows XP finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="375f8-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="375f8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="375f8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="375f8-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="375f8-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




