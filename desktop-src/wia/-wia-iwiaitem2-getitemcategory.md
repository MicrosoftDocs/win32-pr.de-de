---
description: Ruft die Kategorieinformationen eines Elements ab.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'IWiaItem2:: getitemcategory-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344455"
---
# <a name="iwiaitem2getitemcategory-method"></a><span data-ttu-id="fbf74-103">IWiaItem2:: getitemcategory-Methode</span><span class="sxs-lookup"><span data-stu-id="fbf74-103">IWiaItem2::GetItemCategory method</span></span>

<span data-ttu-id="fbf74-104">Ruft die Kategorieinformationen eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="fbf74-104">Gets an item's category information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbf74-105">Syntax</span></span>


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a><span data-ttu-id="fbf74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbf74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf74-107">*pitemcategoryguid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fbf74-107">*pItemCategoryGUID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf74-108">Geben Sie Folgendes ein: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="fbf74-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="fbf74-109">Empfängt einen Zeiger auf die GUID, die die Kategorie des Elements identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fbf74-109">Receives a pointer to the GUID that identifies the category of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf74-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbf74-110">Return value</span></span>

<span data-ttu-id="fbf74-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="fbf74-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="fbf74-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fbf74-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbf74-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fbf74-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbf74-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbf74-114">Remarks</span></span>

<span data-ttu-id="fbf74-115">Jedes [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der hierarchischen Struktur von Objekten, das einem Windows-Abbild Abruf (WIA) 2,0-Hardware Gerät zugeordnet ist, verfügt über eine bestimmte Kategorie.</span><span class="sxs-lookup"><span data-stu-id="fbf74-115">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific category.</span></span> <span data-ttu-id="fbf74-116">Diese Methode ermöglicht es Anwendungen, die Kategorie beliebiger Elemente in einer hierarchischen Struktur von Element Objekten in einem Gerät zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fbf74-116">This method enables applications to identify the category of any item in a hierarchical tree of item objects in a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf74-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbf74-117">Requirements</span></span>



| <span data-ttu-id="fbf74-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbf74-118">Requirement</span></span> | <span data-ttu-id="fbf74-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fbf74-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf74-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbf74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf74-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbf74-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fbf74-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbf74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf74-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbf74-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fbf74-124">Header</span><span class="sxs-lookup"><span data-stu-id="fbf74-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbf74-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf74-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbf74-126">IDL</span><span class="sxs-lookup"><span data-stu-id="fbf74-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fbf74-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fbf74-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 




