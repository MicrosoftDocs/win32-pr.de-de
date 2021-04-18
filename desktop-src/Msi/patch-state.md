---
description: Die State-Eigenschaft gibt den Installationsstatus dieser patchinstanz zurück.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Patch. State (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354754"
---
# <a name="patchstate-property"></a><span data-ttu-id="30ffd-103">Patch. State (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="30ffd-103">Patch.State property</span></span>

<span data-ttu-id="30ffd-104">Die **State** -Eigenschaft gibt den Installationsstatus dieser patchinstanz zurück.</span><span class="sxs-lookup"><span data-stu-id="30ffd-104">The **State** property returns the installation state of this instance of the patch.</span></span>

<span data-ttu-id="30ffd-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="30ffd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ffd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="30ffd-106">Syntax</span></span>


```JScript
propVal = Patch.State
```



## <a name="property-value"></a><span data-ttu-id="30ffd-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="30ffd-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="30ffd-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30ffd-108">Remarks</span></span>

<span data-ttu-id="30ffd-109">Diese Eigenschaft gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="30ffd-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="30ffd-110">Installationsstatus</span><span class="sxs-lookup"><span data-stu-id="30ffd-110">Installation State</span></span>        | <span data-ttu-id="30ffd-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="30ffd-111">Meaning</span></span>                                                      |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="30ffd-112">msipatchstate \_ angewendet</span><span class="sxs-lookup"><span data-stu-id="30ffd-112">MSIPATCHSTATE\_APPLIED</span></span>    | <span data-ttu-id="30ffd-113">Patch wird auf diese Produkt Instanz angewendet.</span><span class="sxs-lookup"><span data-stu-id="30ffd-113">Patch is applied to this product instance.</span></span>                   |
| <span data-ttu-id="30ffd-114">msipatchstate \_ abgelöst</span><span class="sxs-lookup"><span data-stu-id="30ffd-114">MSIPATCHSTATE\_SUPERSEDED</span></span> | <span data-ttu-id="30ffd-115">Patch wird auf diese Produkt Instanz angewendet, aber ersetzt.</span><span class="sxs-lookup"><span data-stu-id="30ffd-115">Patch is applied to this product instance but is superseded.</span></span> |
| <span data-ttu-id="30ffd-116">"msipatchstate" ist \_ veraltet.</span><span class="sxs-lookup"><span data-stu-id="30ffd-116">MSIPATCHSTATE\_OBSOLETED</span></span>  | <span data-ttu-id="30ffd-117">Patch wird in dieser Produkt Instanz, aber veraltet, angewendet.</span><span class="sxs-lookup"><span data-stu-id="30ffd-117">Patch is applied in this product instance but obsolete.</span></span>      |



 

<span data-ttu-id="30ffd-118">Diese Methode kann den Fehler "Unbekannter Patch" zurückgeben \_ \_ , wenn das [**Patch**](patch-object.md) -Objekt mit einer leeren Zeichenfolge für " *ProductCode*" initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="30ffd-118">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ffd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30ffd-119">Requirements</span></span>



| <span data-ttu-id="30ffd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30ffd-120">Requirement</span></span> | <span data-ttu-id="30ffd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="30ffd-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ffd-122">Version</span><span class="sxs-lookup"><span data-stu-id="30ffd-122">Version</span></span><br/> | <span data-ttu-id="30ffd-123">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30ffd-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="30ffd-124">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="30ffd-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="30ffd-125">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="30ffd-125">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="30ffd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="30ffd-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="30ffd-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ffd-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="30ffd-128">IID</span><span class="sxs-lookup"><span data-stu-id="30ffd-128">IID</span></span><br/>     | <span data-ttu-id="30ffd-129">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="30ffd-129">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="30ffd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30ffd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ffd-131">**Patch**</span><span class="sxs-lookup"><span data-stu-id="30ffd-131">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="30ffd-132">**Msigetpatchinfoex**</span><span class="sxs-lookup"><span data-stu-id="30ffd-132">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="30ffd-133">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30ffd-133">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




