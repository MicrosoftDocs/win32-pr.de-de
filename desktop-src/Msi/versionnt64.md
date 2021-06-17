---
description: Das Installationsprogramm legt die VersionNT64-Eigenschaft nur dann auf die Versionsnummer für das Betriebssystem fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262072"
---
# <a name="versionnt64-property"></a><span data-ttu-id="38bd0-103">VersionNT64-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38bd0-103">VersionNT64 property</span></span>

<span data-ttu-id="38bd0-104">Das Installationsprogramm legt die **VersionNT64-Eigenschaft** nur dann auf die Versionsnummer für das Betriebssystem fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38bd0-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="38bd0-105">Die -Eigenschaft ist nicht definiert, wenn das Betriebssystem nicht 64-Bit ist.</span><span class="sxs-lookup"><span data-stu-id="38bd0-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="38bd0-106">Der Wert ist eine ganze Zahl: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="38bd0-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="38bd0-107">Aus Kompatibilitätsgründen ist die -Eigenschaft auch nicht definiert, wenn die [**Template Summary-Eigenschaft**](template-summary.md) angibt, dass das Paket für 32-Bit-Intel-Systeme (x86) gilt und das Betriebssystem keinen 64-Bit-Intel-Code (x64) ausführen kann, z. B. Windows 10 auf ARM (ARM64).</span><span class="sxs-lookup"><span data-stu-id="38bd0-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel (x86) systems and the operating system cannot run 64-bit Intel (x64) code, such as Windows 10 on ARM (ARM64).</span></span>

> [!NOTE]
> <span data-ttu-id="38bd0-108">Ab Windows 10 Build 21277 verfügen ARM64-Builds im Dev-Kanal des Windows Insider Preview Programms über Unterstützung für x64-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="38bd0-108">As of Windows 10 Build 21277, ARM64 builds in the Dev channel of the Windows Insider Preview program have support for x64 applications.</span></span> <span data-ttu-id="38bd0-109">Bei diesen ARM64-Builds wird die VersionNT64-Eigenschaft für x86-Pakete definiert.</span><span class="sxs-lookup"><span data-stu-id="38bd0-109">On these ARM64 builds, the VersionNT64 property is defined for x86 packages.</span></span>

## <a name="remarks"></a><span data-ttu-id="38bd0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38bd0-110">Remarks</span></span>

<span data-ttu-id="38bd0-111">Bedingte Ausdrücke testen für 64-Bit-Windows einfach mithilfe des Eigenschaftennamens oder durch Überprüfen der Version mithilfe eines Vergleichsoperators.</span><span class="sxs-lookup"><span data-stu-id="38bd0-111">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="38bd0-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="38bd0-112">Requirements</span></span>



| <span data-ttu-id="38bd0-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38bd0-113">Requirement</span></span> | <span data-ttu-id="38bd0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="38bd0-114">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38bd0-115">Version</span><span class="sxs-lookup"><span data-stu-id="38bd0-115">Version</span></span><br/> | <span data-ttu-id="38bd0-116">Windows Installer 5.0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38bd0-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="38bd0-117">Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="38bd0-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="38bd0-118">Windows Installer unter Windows Server 2003 oder Windows XP finden Sie unter [Windows Installer Run-Time Requirements (Anforderungen für Windows Installer Run-Time)](windows-installer-portal.md) Informationen zum windows-Mindestdienstpaket, das für eine Windows Installer Version erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="38bd0-118">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38bd0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38bd0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38bd0-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38bd0-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




