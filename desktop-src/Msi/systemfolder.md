---
description: Der Installer legt die SystemFolder-Eigenschaft auf den vollständigen Pfad des System Ordners fest.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: SystemFolder-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366781"
---
# <a name="systemfolder-property"></a><span data-ttu-id="15372-103">SystemFolder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="15372-103">SystemFolder property</span></span>

<span data-ttu-id="15372-104">Der Installer legt die **SystemFolder** -Eigenschaft auf den vollständigen Pfad des System Ordners fest.</span><span class="sxs-lookup"><span data-stu-id="15372-104">The installer sets the **SystemFolder** property to the full path of the System folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="15372-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15372-105">Remarks</span></span>

<span data-ttu-id="15372-106">Diese Eigenschaft wird vom Installationsprogramm festgelegt.</span><span class="sxs-lookup"><span data-stu-id="15372-106">The installer sets this property.</span></span> <span data-ttu-id="15372-107">Beispielsweise kann auf 32-Bit-Fenstern der Wert "C: \\ Windows \\ system32" lauten.</span><span class="sxs-lookup"><span data-stu-id="15372-107">For example, on 32-bit Windows the value may be C:\\Windows\\System32.</span></span> <span data-ttu-id="15372-108">Auf 64-Bit-Fenstern kann der Wert "C: \\ Windows \\ syswow64" lauten.</span><span class="sxs-lookup"><span data-stu-id="15372-108">On 64-bit Windows, the value may be C:\\Windows\\SysWow64.</span></span>

<span data-ttu-id="15372-109">Dieser Ordner ist normalerweise ein Unterverzeichnis des Windows-Ordners.</span><span class="sxs-lookup"><span data-stu-id="15372-109">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="15372-110">Sie befindet sich jedoch auf einem Server, wenn Sie für freigegebene Fenster konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="15372-110">However, it resides on a server when configured for Shared Windows.</span></span>

<span data-ttu-id="15372-111">Dieser Ordner ist lokal, auch wenn er für freigegebene Fenster konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="15372-111">This folder is local, even when configured for shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="15372-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15372-112">Requirements</span></span>



| <span data-ttu-id="15372-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15372-113">Requirement</span></span> | <span data-ttu-id="15372-114">Wert</span><span class="sxs-lookup"><span data-stu-id="15372-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15372-115">Version</span><span class="sxs-lookup"><span data-stu-id="15372-115">Version</span></span><br/> | <span data-ttu-id="15372-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="15372-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="15372-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15372-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="15372-118">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="15372-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="15372-119">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="15372-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15372-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15372-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15372-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15372-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




