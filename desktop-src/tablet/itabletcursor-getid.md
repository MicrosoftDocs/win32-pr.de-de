---
description: Ruft den tablettstiftbezeichner ab.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'Itabletcursor:: GetId-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393718"
---
# <a name="itabletcursorgetid-method"></a><span data-ttu-id="86b55-103">Itabletcursor:: GetId-Methode</span><span class="sxs-lookup"><span data-stu-id="86b55-103">ITabletCursor::GetId method</span></span>

<span data-ttu-id="86b55-104">Ruft den tablettstiftbezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="86b55-104">Retrieves the stylus identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="86b55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86b55-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a><span data-ttu-id="86b55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86b55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b55-107">*pcId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="86b55-107">*pCid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86b55-108">Der Bezeichner des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="86b55-108">The identifier of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b55-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86b55-109">Return value</span></span>

<span data-ttu-id="86b55-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="86b55-110">This method can return one of these values.</span></span>



| <span data-ttu-id="86b55-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="86b55-111">Return code</span></span>                                                                            | <span data-ttu-id="86b55-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86b55-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="86b55-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86b55-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="86b55-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="86b55-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="86b55-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="86b55-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="86b55-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="86b55-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86b55-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86b55-117">Remarks</span></span>

<span data-ttu-id="86b55-118">Die Cursor- \_ ID ist als DWORD definiert.</span><span class="sxs-lookup"><span data-stu-id="86b55-118">CURSOR\_ID is defined as a DWORD.</span></span>

## <a name="requirements"></a><span data-ttu-id="86b55-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86b55-119">Requirements</span></span>



| <span data-ttu-id="86b55-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86b55-120">Requirement</span></span> | <span data-ttu-id="86b55-121">Wert</span><span class="sxs-lookup"><span data-stu-id="86b55-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86b55-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86b55-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86b55-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86b55-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="86b55-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86b55-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86b55-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="86b55-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="86b55-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86b55-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="86b55-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="86b55-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86b55-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86b55-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b55-129">**Itabletcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="86b55-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




