---
description: Die Media Disks-Eigenschaft listet alle Medien Datenträger für diese Produkt Instanz auf. Diese Eigenschaft ruft msisourcelistenumschlag mediadisks auf. Gibt die Datenträger Informationen als Array von Datensatz-Objekten zurück.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Product. mediadisks (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e07af832837aaeb77759816c08cf68d04e14c255
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360342"
---
# <a name="productmediadisks-property"></a><span data-ttu-id="0605e-105">Product. mediadisks (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0605e-105">Product.MediaDisks property</span></span>

<span data-ttu-id="0605e-106">Die Media **Disks** -Eigenschaft listet alle Medien Datenträger für diese Produkt Instanz auf.</span><span class="sxs-lookup"><span data-stu-id="0605e-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="0605e-107">Diese Eigenschaft ruft [**msisourcelistenumschlag mediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)auf.</span><span class="sxs-lookup"><span data-stu-id="0605e-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="0605e-108">Gibt die Datenträger Informationen als Array von [**Datensatz**](record-object.md) -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="0605e-108">Returns the disk information as an array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="0605e-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0605e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0605e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0605e-110">Syntax</span></span>


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="0605e-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0605e-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0605e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0605e-112">Remarks</span></span>

<span data-ttu-id="0605e-113">In jedem Datensatz enthält das erste Feld die Datenträger-ID, das zweite Feld enthält die Volumebezeichnung, und das dritte Feld enthält die für den Datenträger registrierte Datenträger Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="0605e-113">In each record, the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="0605e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0605e-114">Requirements</span></span>



| <span data-ttu-id="0605e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0605e-115">Requirement</span></span> | <span data-ttu-id="0605e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0605e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0605e-117">Version</span><span class="sxs-lookup"><span data-stu-id="0605e-117">Version</span></span><br/> | <span data-ttu-id="0605e-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0605e-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0605e-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0605e-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0605e-120">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0605e-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="0605e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0605e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="0605e-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0605e-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="0605e-123">IID</span><span class="sxs-lookup"><span data-stu-id="0605e-123">IID</span></span><br/>     | <span data-ttu-id="0605e-124">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0605e-124">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="0605e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0605e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0605e-126">**Product**</span><span class="sxs-lookup"><span data-stu-id="0605e-126">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="0605e-127">**Msisourcelistenumschlag mediadisks**</span><span class="sxs-lookup"><span data-stu-id="0605e-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="0605e-128">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0605e-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




