---
description: Der Installer legt die CommonFiles64Folder-Eigenschaft auf den vollständigen Pfad des vordefinierten 64-Bit-Ordners für allgemeine Dateien fest. Die vorhandene CommonFilesFolder-Eigenschaft wird auf den entsprechenden 32-Bit-Ordner festgelegt.
ms.assetid: 6730170a-0f73-4a84-b3fb-bd15c72917c7
title: CommonFiles64Folder-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44a6720e609cfa79cd0e4adbfd5136c7a92a5ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368451"
---
# <a name="commonfiles64folder-property"></a><span data-ttu-id="099a6-104">CommonFiles64Folder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="099a6-104">CommonFiles64Folder property</span></span>

<span data-ttu-id="099a6-105">Der Installer legt die **CommonFiles64Folder** -Eigenschaft auf den vollständigen Pfad des vordefinierten 64-Bit-Ordners für allgemeine Dateien fest.</span><span class="sxs-lookup"><span data-stu-id="099a6-105">The installer sets the **CommonFiles64Folder** property to the full path of the predefined 64-bit Common Files folder.</span></span> <span data-ttu-id="099a6-106">Die vorhandene [**CommonFilesFolder**](commonfilesfolder.md) -Eigenschaft wird auf den entsprechenden 32-Bit-Ordner festgelegt.</span><span class="sxs-lookup"><span data-stu-id="099a6-106">The existing [**CommonFilesFolder**](commonfilesfolder.md) property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="099a6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="099a6-107">Remarks</span></span>

<span data-ttu-id="099a6-108">Das Installationsprogramm legt diese Eigenschaft auf 64-Bit-Fenstern fest.</span><span class="sxs-lookup"><span data-stu-id="099a6-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="099a6-109">Diese Eigenschaft wird auf 32-Bit-Fenstern nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="099a6-109">This property is not used on 32-bit Windows.</span></span> <span data-ttu-id="099a6-110">Bei Verwendung von 64-Bit-Fenstern ist der Wert möglicherweise "C: \\ Dateien für \\ Allgemeine Dateien".</span><span class="sxs-lookup"><span data-stu-id="099a6-110">When using 64-bit Windows, the value may be "C:\\Program Files\\Common Files".</span></span>

## <a name="requirements"></a><span data-ttu-id="099a6-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="099a6-111">Requirements</span></span>



| <span data-ttu-id="099a6-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="099a6-112">Requirement</span></span> | <span data-ttu-id="099a6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="099a6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="099a6-114">Version</span><span class="sxs-lookup"><span data-stu-id="099a6-114">Version</span></span><br/> | <span data-ttu-id="099a6-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="099a6-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="099a6-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="099a6-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="099a6-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="099a6-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="099a6-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="099a6-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="099a6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="099a6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099a6-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="099a6-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




