---
description: Gibt eine Zeichenfolge zurück, die den Namen des Tablettgeräts enthält.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: 'ITablet:: GetName-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c2d6bd20a011b1bf5cfbe7582445de45728bbd7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216410"
---
# <a name="itabletgetname-method"></a><span data-ttu-id="fd54f-103">ITablet:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="fd54f-103">ITablet::GetName method</span></span>

<span data-ttu-id="fd54f-104">Gibt eine Zeichenfolge zurück, die den Namen des Tablettgeräts enthält.</span><span class="sxs-lookup"><span data-stu-id="fd54f-104">Returns a string containing the name of the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd54f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd54f-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="fd54f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd54f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd54f-107">*ppwszname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fd54f-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd54f-108">Zeiger auf eine Zeichenfolge, die den Namen des Tablettgeräts enthält.</span><span class="sxs-lookup"><span data-stu-id="fd54f-108">Pointer to a string containing the name of the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd54f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd54f-109">Return value</span></span>

<span data-ttu-id="fd54f-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fd54f-110">This method can return one of these values.</span></span>



| <span data-ttu-id="fd54f-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fd54f-111">Return code</span></span>                                                                            | <span data-ttu-id="fd54f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd54f-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="fd54f-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd54f-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="fd54f-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="fd54f-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="fd54f-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="fd54f-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="fd54f-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="fd54f-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd54f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd54f-117">Remarks</span></span>

<span data-ttu-id="fd54f-118">Es ist Aufgabe des Aufrufers, den von dieser Methode zurückgegebenen Speicher mithilfe von " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)" freizugeben.</span><span class="sxs-lookup"><span data-stu-id="fd54f-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd54f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd54f-119">Requirements</span></span>



| <span data-ttu-id="fd54f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd54f-120">Requirement</span></span> | <span data-ttu-id="fd54f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fd54f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd54f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd54f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd54f-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd54f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fd54f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd54f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd54f-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd54f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fd54f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd54f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd54f-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd54f-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd54f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd54f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd54f-129">**ITablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fd54f-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

