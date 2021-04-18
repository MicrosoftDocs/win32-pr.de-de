---
description: Die patchesex-Eigenschaft gibt ein RecordList-Objekt zurück, das die Liste der Patches auflistet.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Installer. patchesex-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368308"
---
# <a name="installerpatchesex-property"></a><span data-ttu-id="c543f-103">Installer. patchesex-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c543f-103">Installer.PatchesEx property</span></span>

<span data-ttu-id="c543f-104">Die **patchesex** -Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das die Liste der Patches auflistet.</span><span class="sxs-lookup"><span data-stu-id="c543f-104">The **PatchesEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of patches.</span></span> <span data-ttu-id="c543f-105">Diese Eigenschaft ruft [**msienumschlag Patch esex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)auf.</span><span class="sxs-lookup"><span data-stu-id="c543f-105">This property calls [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span>

<span data-ttu-id="c543f-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c543f-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c543f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c543f-107">Syntax</span></span>


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a><span data-ttu-id="c543f-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c543f-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="c543f-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c543f-109">Requirements</span></span>



| <span data-ttu-id="c543f-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c543f-110">Requirement</span></span> | <span data-ttu-id="c543f-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c543f-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c543f-112">Version</span><span class="sxs-lookup"><span data-stu-id="c543f-112">Version</span></span><br/> | <span data-ttu-id="c543f-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c543f-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c543f-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c543f-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c543f-115">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c543f-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="c543f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="c543f-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="c543f-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c543f-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="c543f-118">IID</span><span class="sxs-lookup"><span data-stu-id="c543f-118">IID</span></span><br/>     | <span data-ttu-id="c543f-119">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c543f-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="c543f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c543f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c543f-121">**Installationsprogramm**</span><span class="sxs-lookup"><span data-stu-id="c543f-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="c543f-122">**Msienum patchesex**</span><span class="sxs-lookup"><span data-stu-id="c543f-122">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="c543f-123">**Patch**</span><span class="sxs-lookup"><span data-stu-id="c543f-123">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="c543f-124">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c543f-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




