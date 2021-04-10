---
description: Ruft ein Rechteck ab, das den maximalen Eingabebereich des Tablets darstellt.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'ITablet:: getmaxinputrect-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: de2649fe7410e6d335f653c09bfe86a8ddaac813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867099"
---
# <a name="itabletgetmaxinputrect-method"></a><span data-ttu-id="090e4-103">ITablet:: getmaxinputrect-Methode</span><span class="sxs-lookup"><span data-stu-id="090e4-103">ITablet::GetMaxInputRect method</span></span>

<span data-ttu-id="090e4-104">Ruft ein Rechteck ab, das den maximalen Eingabebereich des Tablets darstellt.</span><span class="sxs-lookup"><span data-stu-id="090e4-104">Retrieves a rectangle that represents maximum input area of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="090e4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="090e4-105">Syntax</span></span>


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="090e4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="090e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090e4-107">*prcinput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="090e4-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="090e4-108">Zeiger auf das Rechteck, das den maximalen Eingabebereich des Tablets darstellt.</span><span class="sxs-lookup"><span data-stu-id="090e4-108">Pointer to rectangle that represents maximum input area of the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090e4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="090e4-109">Return value</span></span>

<span data-ttu-id="090e4-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="090e4-110">This method can return one of these values.</span></span>



| <span data-ttu-id="090e4-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="090e4-111">Return code</span></span>                                                                            | <span data-ttu-id="090e4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="090e4-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="090e4-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="090e4-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="090e4-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="090e4-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="090e4-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="090e4-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="090e4-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="090e4-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="090e4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="090e4-117">Requirements</span></span>



| <span data-ttu-id="090e4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="090e4-118">Requirement</span></span> | <span data-ttu-id="090e4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="090e4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="090e4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="090e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="090e4-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="090e4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="090e4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="090e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="090e4-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="090e4-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="090e4-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="090e4-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="090e4-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="090e4-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="090e4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="090e4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090e4-127">**ITablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="090e4-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




