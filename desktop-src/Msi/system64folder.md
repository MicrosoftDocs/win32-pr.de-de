---
description: Der Installer legt die System64Folder-Eigenschaft auf den vollständigen Pfad zum vordefinierten System64-Ordner fest. Die vorhandene System64Folder-Eigenschaft wird auf den entsprechenden 32-Bit-Ordner festgelegt.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: System64Folder-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371535"
---
# <a name="system64folder-property"></a><span data-ttu-id="9d0a6-104">System64Folder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9d0a6-104">System64Folder property</span></span>

<span data-ttu-id="9d0a6-105">Der Installer legt die **System64Folder** -Eigenschaft auf den vollständigen Pfad zum vordefinierten System64-Ordner fest.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-105">The installer sets the **System64Folder** property to the full path to the predefined System64 folder.</span></span> <span data-ttu-id="9d0a6-106">Die vorhandene **System64Folder** -Eigenschaft wird auf den entsprechenden 32-Bit-Ordner festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-106">The existing **System64Folder** property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d0a6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d0a6-107">Remarks</span></span>

<span data-ttu-id="9d0a6-108">Das Installationsprogramm legt diese Eigenschaft auf 64-Bit-Fenstern fest.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="9d0a6-109">Beispielsweise kann auf 64-Bit-Fenstern der Wert C: \\ Fenster System32 lauten \\ .</span><span class="sxs-lookup"><span data-stu-id="9d0a6-109">For example, on 64-bit Windows, the value may be C:\\Window\\System32.</span></span> <span data-ttu-id="9d0a6-110">Diese Eigenschaft wird auf 32-Bit-Fenstern nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-110">This property is not used on 32-bit Windows.</span></span>

<span data-ttu-id="9d0a6-111">Dieser Ordner ist normalerweise ein Unterverzeichnis des Windows-Ordners.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-111">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="9d0a6-112">Sie befindet sich jedoch auf einem Server, wenn Sie für freigegebene Fenster konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-112">However, it resides on a server when configured for Shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d0a6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d0a6-113">Requirements</span></span>



| <span data-ttu-id="9d0a6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d0a6-114">Requirement</span></span> | <span data-ttu-id="9d0a6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9d0a6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0a6-116">Version</span><span class="sxs-lookup"><span data-stu-id="9d0a6-116">Version</span></span><br/> | <span data-ttu-id="9d0a6-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9d0a6-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9d0a6-119">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9d0a6-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9d0a6-120">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9d0a6-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d0a6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d0a6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d0a6-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d0a6-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




