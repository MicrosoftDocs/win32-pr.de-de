---
description: Die Media Disks-Eigenschaft listet alle Medien Datenträger für diese Produkt Instanz auf. Diese Eigenschaft ruft msisourcelistenumschlag mediadisks auf. Gibt die Datenträger Informationen als Array von Datensatz-Objekten zurück.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Patch. mediadisks (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369385"
---
# <a name="patchmediadisks-property"></a><span data-ttu-id="70880-105">Patch. mediadisks (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="70880-105">Patch.MediaDisks property</span></span>

<span data-ttu-id="70880-106">Die Media **Disks** -Eigenschaft listet alle Medien Datenträger für diese Produkt Instanz auf.</span><span class="sxs-lookup"><span data-stu-id="70880-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="70880-107">Diese Eigenschaft ruft [**msisourcelistenumschlag mediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)auf.</span><span class="sxs-lookup"><span data-stu-id="70880-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="70880-108">Gibt die Datenträger Informationen als Array von [**Datensatz**](record-object.md) -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="70880-108">Returns the disk information as array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="70880-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="70880-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="70880-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="70880-110">Syntax</span></span>


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="70880-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="70880-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="70880-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70880-112">Remarks</span></span>

<span data-ttu-id="70880-113">In jedem Datensatz enthält das erste Feld die Datenträger-ID, das zweite Feld enthält die Volumebezeichnung, und das dritte Feld enthält die für den Datenträger registrierte Datenträger Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="70880-113">In each record the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="70880-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70880-114">Requirements</span></span>



| <span data-ttu-id="70880-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70880-115">Requirement</span></span> | <span data-ttu-id="70880-116">Wert</span><span class="sxs-lookup"><span data-stu-id="70880-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70880-117">Version</span><span class="sxs-lookup"><span data-stu-id="70880-117">Version</span></span><br/> | <span data-ttu-id="70880-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70880-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="70880-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="70880-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="70880-120">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="70880-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="70880-121">DLL</span><span class="sxs-lookup"><span data-stu-id="70880-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="70880-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70880-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="70880-123">IID</span><span class="sxs-lookup"><span data-stu-id="70880-123">IID</span></span><br/>     | <span data-ttu-id="70880-124">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="70880-124">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="70880-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70880-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70880-126">**Patch**</span><span class="sxs-lookup"><span data-stu-id="70880-126">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="70880-127">**Msisourcelistenumschlag mediadisks**</span><span class="sxs-lookup"><span data-stu-id="70880-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="70880-128">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="70880-128">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="70880-129">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="70880-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




