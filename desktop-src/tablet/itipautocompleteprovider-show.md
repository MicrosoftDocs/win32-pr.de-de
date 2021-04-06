---
description: Hiermit wird die Liste der Auto Vervollständigen angezeigt oder ausgeblendet.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'Itipaudecompleteprovider:: Show-Methode (tipaudecomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759816"
---
# <a name="itipautocompleteprovidershow-method"></a><span data-ttu-id="8ad62-103">Itipaudecompleteprovider:: Show-Methode</span><span class="sxs-lookup"><span data-stu-id="8ad62-103">ITipAutocompleteProvider::Show method</span></span>

<span data-ttu-id="8ad62-104">Hiermit wird die Liste der Auto Vervollständigen angezeigt oder ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="8ad62-104">Displays or hides the auto complete list.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad62-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ad62-105">Syntax</span></span>


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a><span data-ttu-id="8ad62-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ad62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ad62-107">mit der Bezeichnung  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ad62-107">*fShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad62-108">**True** , um die Benutzeroberfläche für die automatische Vervollständigung anzuzeigen, **false** , um die Benutzeroberfläche für die automatische Vervollständigung zu blenden.</span><span class="sxs-lookup"><span data-stu-id="8ad62-108">**TRUE** to show the auto complete user interface, **FALSE** to hide the auto complete list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ad62-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ad62-109">Return value</span></span>

<span data-ttu-id="8ad62-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8ad62-110">This method can return one of these values.</span></span>



| <span data-ttu-id="8ad62-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8ad62-111">Return code</span></span>                                                                            | <span data-ttu-id="8ad62-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ad62-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8ad62-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ad62-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8ad62-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="8ad62-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8ad62-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="8ad62-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8ad62-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8ad62-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ad62-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ad62-117">Remarks</span></span>

<span data-ttu-id="8ad62-118">Diese Methode wird vom Client aufgerufen, um die Auto Vervollständigen-Liste anzuzeigen oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="8ad62-118">This method is called by the client to show or hide the auto complete list.</span></span> <span data-ttu-id="8ad62-119">Wenn die Auto Vervollständigen-Liste nicht angezeigt wird  und der Ausdruck **false** ist, führt diese Methode keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8ad62-119">If the auto complete list is not displayed and *fShow* is **FALSE**, this method does nothing.</span></span> <span data-ttu-id="8ad62-120">Wenn die Auto Vervollständigen-Liste angezeigt wird und die Angabe von " *f* " **true** ist, führt diese Methode keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8ad62-120">If the auto complete list is displayed and *fShow* is **TRUE**, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ad62-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ad62-121">Requirements</span></span>



| <span data-ttu-id="8ad62-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ad62-122">Requirement</span></span> | <span data-ttu-id="8ad62-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8ad62-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad62-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ad62-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8ad62-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ad62-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="8ad62-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ad62-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8ad62-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8ad62-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="8ad62-128">Header</span><span class="sxs-lookup"><span data-stu-id="8ad62-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ad62-129"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="8ad62-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8ad62-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8ad62-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ad62-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ad62-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="8ad62-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ad62-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad62-133">**Itipauescompleteprovider-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8ad62-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="8ad62-134">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="8ad62-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




