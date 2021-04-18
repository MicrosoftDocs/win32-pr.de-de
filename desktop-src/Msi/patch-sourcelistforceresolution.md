---
description: Die sourcelistforceresolution-Methode löscht die zuletzt verwendete Source-Eigenschaft.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Patch. sourcelistforceresolution-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364855"
---
# <a name="patchsourcelistforceresolution-method"></a><span data-ttu-id="6069d-103">Patch. sourcelistforceresolution-Methode</span><span class="sxs-lookup"><span data-stu-id="6069d-103">Patch.SourceListForceResolution method</span></span>

<span data-ttu-id="6069d-104">Die **sourcelistforceresolution** -Methode löscht die zuletzt verwendete Source-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6069d-104">The **SourceListForceResolution** method clears the last used source property.</span></span> <span data-ttu-id="6069d-105">Dadurch wird das Installationsprogramm gezwungen, die Quell Liste nach einer gültigen patchquelle zu durchsuchen, wenn die patchquelle das nächste Mal benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="6069d-105">This forces the installer to search the source list for a valid patch source the next time the patch source is required.</span></span> <span data-ttu-id="6069d-106">Das Installationsprogramm erfordert beispielsweise, dass die patchquelle eine Installation oder Neuinstallation ausführt, wenn die lokale Cache Kopie des Patches fehlt.</span><span class="sxs-lookup"><span data-stu-id="6069d-106">For example, the installer requires the patch source to perform an installation or reinstallation when the local cache copy of the patch is missing.</span></span> <span data-ttu-id="6069d-107">Diese Methode ruft [**msisourcelistforceresolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)auf.</span><span class="sxs-lookup"><span data-stu-id="6069d-107">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="6069d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6069d-108">Syntax</span></span>


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="6069d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6069d-109">Parameters</span></span>

<span data-ttu-id="6069d-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6069d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6069d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6069d-111">Return value</span></span>

<span data-ttu-id="6069d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6069d-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6069d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6069d-113">Requirements</span></span>



| <span data-ttu-id="6069d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6069d-114">Requirement</span></span> | <span data-ttu-id="6069d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6069d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6069d-116">Version</span><span class="sxs-lookup"><span data-stu-id="6069d-116">Version</span></span><br/> | <span data-ttu-id="6069d-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6069d-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6069d-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6069d-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6069d-119">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6069d-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="6069d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6069d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="6069d-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6069d-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="6069d-122">IID</span><span class="sxs-lookup"><span data-stu-id="6069d-122">IID</span></span><br/>     | <span data-ttu-id="6069d-123">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6069d-123">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="6069d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6069d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6069d-125">**Patch**</span><span class="sxs-lookup"><span data-stu-id="6069d-125">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="6069d-126">**Msisourcelistforceresolution**</span><span class="sxs-lookup"><span data-stu-id="6069d-126">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="6069d-127">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6069d-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




