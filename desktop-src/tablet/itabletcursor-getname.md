---
description: Ruft den Namen des Tablettstifts ab.
ms.assetid: 94955c04-f699-428b-b4bf-53919b61b1ab
title: 'Itabletcursor:: GetName-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b9d984d5eb711c2344ba0f9fb2dbf410a7d49bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960666"
---
# <a name="itabletcursorgetname-method"></a><span data-ttu-id="25771-103">Itabletcursor:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="25771-103">ITabletCursor::GetName method</span></span>

<span data-ttu-id="25771-104">Ruft den Namen des Tablettstifts ab.</span><span class="sxs-lookup"><span data-stu-id="25771-104">Retrieves the name of the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="25771-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25771-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="25771-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25771-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25771-107">*ppwszname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="25771-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25771-108">Der Name des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="25771-108">The name of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25771-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25771-109">Return value</span></span>

<span data-ttu-id="25771-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="25771-110">This method can return one of these values.</span></span>



| <span data-ttu-id="25771-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="25771-111">Return code</span></span>                                                                            | <span data-ttu-id="25771-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25771-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="25771-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25771-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="25771-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="25771-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="25771-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="25771-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="25771-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="25771-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25771-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25771-117">Remarks</span></span>

<span data-ttu-id="25771-118">Es ist Aufgabe des Aufrufers, den von dieser Methode zurückgegebenen Speicher mithilfe von " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)" freizugeben.</span><span class="sxs-lookup"><span data-stu-id="25771-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="25771-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25771-119">Requirements</span></span>



| <span data-ttu-id="25771-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25771-120">Requirement</span></span> | <span data-ttu-id="25771-121">Wert</span><span class="sxs-lookup"><span data-stu-id="25771-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25771-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25771-122">Minimum supported client</span></span><br/> | <span data-ttu-id="25771-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25771-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="25771-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25771-124">Minimum supported server</span></span><br/> | <span data-ttu-id="25771-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="25771-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="25771-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25771-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="25771-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25771-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25771-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25771-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25771-129">**Itabletcursor**</span><span class="sxs-lookup"><span data-stu-id="25771-129">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="25771-130">**Itabletcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="25771-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

