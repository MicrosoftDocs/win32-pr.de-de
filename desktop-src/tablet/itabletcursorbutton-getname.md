---
description: Ruft den Namen der Tablettstiftschaltfläche ab.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: 'Itabletcurrsorbutton:: GetName-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347421"
---
# <a name="itabletcursorbuttongetname-method"></a><span data-ttu-id="ff4c9-103">Itabletcurrsorbutton:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="ff4c9-103">ITabletCursorButton::GetName method</span></span>

<span data-ttu-id="ff4c9-104">Ruft den Namen der Tablettstiftschaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="ff4c9-104">Retrieves the name of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff4c9-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="ff4c9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff4c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff4c9-107">*ppwszname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ff4c9-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff4c9-108">Der Name der Tablettstiftschaltfläche.</span><span class="sxs-lookup"><span data-stu-id="ff4c9-108">The name of the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff4c9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff4c9-109">Return value</span></span>

<span data-ttu-id="ff4c9-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ff4c9-110">This method can return one of these values.</span></span>



| <span data-ttu-id="ff4c9-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ff4c9-111">Return code</span></span>                                                                            | <span data-ttu-id="ff4c9-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff4c9-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ff4c9-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ff4c9-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ff4c9-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ff4c9-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="ff4c9-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="ff4c9-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ff4c9-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ff4c9-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ff4c9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff4c9-117">Remarks</span></span>

<span data-ttu-id="ff4c9-118">Es ist Aufgabe des Aufrufers, den von dieser Methode zurückgegebenen Speicher mithilfe von " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)" freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ff4c9-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff4c9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff4c9-119">Requirements</span></span>



| <span data-ttu-id="ff4c9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff4c9-120">Requirement</span></span> | <span data-ttu-id="ff4c9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ff4c9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4c9-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ff4c9-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff4c9-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ff4c9-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff4c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ff4c9-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ff4c9-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ff4c9-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff4c9-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff4c9-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff4c9-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff4c9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff4c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff4c9-129">**Itabletcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ff4c9-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

