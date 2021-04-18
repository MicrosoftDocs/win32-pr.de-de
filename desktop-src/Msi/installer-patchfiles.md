---
description: Die PATCHFILES-Eigenschaft gibt ein stringlist-Objekt zurück, das eine Liste von Dateien enthält, die durch die bereitgestellte Liste der Patches aktualisiert werden können.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Installer. PATCHFILES (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358774"
---
# <a name="installerpatchfiles-property"></a><span data-ttu-id="69cff-103">Installer. PATCHFILES (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="69cff-103">Installer.PatchFiles property</span></span>

<span data-ttu-id="69cff-104">Die **PATCHFILES** -Eigenschaft gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das eine Liste von Dateien enthält, die durch die bereitgestellte Liste der Patches aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="69cff-104">The **PatchFiles** property returns a [**StringList**](stringlist-object.md) object that contains a list of files that can be updated by the provided list of patches.</span></span> <span data-ttu-id="69cff-105">Diese Eigenschaft ruft [**msigetpatchfilelist**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)auf.</span><span class="sxs-lookup"><span data-stu-id="69cff-105">This property calls [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="69cff-106">Weitere Informationen zum Verwenden der **PATCHFILES** -Eigenschaft finden Sie [unter Auflisten der Dateien, die aktualisiert werden können](listing-the-files-that-can-be-updated.md).</span><span class="sxs-lookup"><span data-stu-id="69cff-106">For more information about using the **PatchFiles** property see [Listing the Files that can be Updated](listing-the-files-that-can-be-updated.md).</span></span>

<span data-ttu-id="69cff-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="69cff-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="69cff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="69cff-108">Syntax</span></span>


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a><span data-ttu-id="69cff-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="69cff-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="69cff-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69cff-110">Requirements</span></span>



| <span data-ttu-id="69cff-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69cff-111">Requirement</span></span> | <span data-ttu-id="69cff-112">Wert</span><span class="sxs-lookup"><span data-stu-id="69cff-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69cff-113">Version</span><span class="sxs-lookup"><span data-stu-id="69cff-113">Version</span></span><br/> | <span data-ttu-id="69cff-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="69cff-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="69cff-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="69cff-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="69cff-116">Windows Installer 4,5 unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="69cff-116">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="69cff-117">DLL</span><span class="sxs-lookup"><span data-stu-id="69cff-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="69cff-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69cff-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="69cff-119">IID</span><span class="sxs-lookup"><span data-stu-id="69cff-119">IID</span></span><br/>     | <span data-ttu-id="69cff-120">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="69cff-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="69cff-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69cff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69cff-122">**Installer-Objekt**</span><span class="sxs-lookup"><span data-stu-id="69cff-122">**Installer Object**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="69cff-123">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="69cff-123">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




