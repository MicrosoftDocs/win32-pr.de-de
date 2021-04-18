---
description: Die sourcelistclearall-Methode des Patch-Objekts löscht die vollständige Quell Liste aller Quellen des angegebenen Typs für einen Patch. Akzeptiert den Typ als Parameter. Diese Methode ruft msisourcelistclearallex auf.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Patch. sourcelistclearall-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351385"
---
# <a name="patchsourcelistclearall-method"></a><span data-ttu-id="b1097-105">Patch. sourcelistclearall-Methode</span><span class="sxs-lookup"><span data-stu-id="b1097-105">Patch.SourceListClearAll method</span></span>

<span data-ttu-id="b1097-106">Die **sourcelistclearall** -Methode des [**Patch**](patch-object.md) -Objekts löscht die vollständige Quell Liste aller Quellen des angegebenen Typs für einen Patch.</span><span class="sxs-lookup"><span data-stu-id="b1097-106">The **SourceListClearAll** method of the [**Patch**](patch-object.md) object clears the complete source list of all sources of the specified type for a patch.</span></span> <span data-ttu-id="b1097-107">Akzeptiert den *Typ* als Parameter.</span><span class="sxs-lookup"><span data-stu-id="b1097-107">Accepts *Type* as a parameter.</span></span> <span data-ttu-id="b1097-108">Diese Methode ruft [**msisourcelistclearallex**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)auf.</span><span class="sxs-lookup"><span data-stu-id="b1097-108">This method calls [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1097-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1097-109">Syntax</span></span>


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="b1097-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1097-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1097-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="b1097-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="b1097-112">Der Typ des Quell Typs, z. b. Netzwerk, URL oder Medien.</span><span class="sxs-lookup"><span data-stu-id="b1097-112">The type of source type, such as network, URL or media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1097-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1097-113">Return value</span></span>

<span data-ttu-id="b1097-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b1097-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1097-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1097-115">Requirements</span></span>



| <span data-ttu-id="b1097-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1097-116">Requirement</span></span> | <span data-ttu-id="b1097-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b1097-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1097-118">Version</span><span class="sxs-lookup"><span data-stu-id="b1097-118">Version</span></span><br/> | <span data-ttu-id="b1097-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b1097-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b1097-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b1097-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b1097-121">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1097-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="b1097-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b1097-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1097-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1097-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="b1097-124">IID</span><span class="sxs-lookup"><span data-stu-id="b1097-124">IID</span></span><br/>     | <span data-ttu-id="b1097-125">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b1097-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="b1097-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1097-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1097-127">**Patch**</span><span class="sxs-lookup"><span data-stu-id="b1097-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="b1097-128">**Msisourcelistclearallex**</span><span class="sxs-lookup"><span data-stu-id="b1097-128">**MsiSourceListClearAllEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[<span data-ttu-id="b1097-129">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1097-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




