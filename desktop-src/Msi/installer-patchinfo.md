---
description: Die schreibgeschützte patchinfo-Eigenschaft des Installer-Objekts gibt Informationen zu einem Patch zurück.
ms.assetid: a92e409e-b4a5-42cc-a87d-239c23655e5e
title: Installer. patchinfo (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7105c872b453877876e92a7cf6710a71bd1ed5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373996"
---
# <a name="installerpatchinfo-property"></a><span data-ttu-id="54db2-103">Installer. patchinfo (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="54db2-103">Installer.PatchInfo property</span></span>

<span data-ttu-id="54db2-104">Die schreibgeschützte **patchinfo** -Eigenschaft des [**Installer**](installer-object.md) -Objekts gibt Informationen zu einem Patch zurück.</span><span class="sxs-lookup"><span data-stu-id="54db2-104">The read-only **PatchInfo** property of the [**Installer**](installer-object.md) object returns information about a patch.</span></span>

<span data-ttu-id="54db2-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="54db2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54db2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="54db2-106">Syntax</span></span>


```JScript
propVal = Installer.PatchInfo
```



## <a name="property-value"></a><span data-ttu-id="54db2-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="54db2-107">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="54db2-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54db2-108">Requirements</span></span>



| <span data-ttu-id="54db2-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54db2-109">Requirement</span></span> | <span data-ttu-id="54db2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="54db2-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54db2-111">Version</span><span class="sxs-lookup"><span data-stu-id="54db2-111">Version</span></span><br/> | <span data-ttu-id="54db2-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54db2-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="54db2-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54db2-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="54db2-114">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="54db2-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="54db2-115">DLL</span><span class="sxs-lookup"><span data-stu-id="54db2-115">DLL</span></span><br/>     | <dl> <span data-ttu-id="54db2-116"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54db2-116"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="54db2-117">IID</span><span class="sxs-lookup"><span data-stu-id="54db2-117">IID</span></span><br/>     | <span data-ttu-id="54db2-118">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="54db2-118">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="54db2-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54db2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54db2-120">**Msigetpatchinfo**</span><span class="sxs-lookup"><span data-stu-id="54db2-120">**MsiGetPatchInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)
</dt> </dl>

 

 




