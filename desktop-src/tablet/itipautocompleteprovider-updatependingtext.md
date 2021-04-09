---
description: Wird vom Auto Vervollständigen-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich eingegeben hat.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'Itipaudecompleteprovider:: updatependingtext-Methode (tipaudecomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050580"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a><span data-ttu-id="15d13-103">Itipaudecompleteprovider:: updatependingtext-Methode</span><span class="sxs-lookup"><span data-stu-id="15d13-103">ITipAutocompleteProvider::UpdatePendingText method</span></span>

<span data-ttu-id="15d13-104">Wird vom Auto Vervollständigen-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="15d13-104">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d13-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15d13-105">Syntax</span></span>


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a><span data-ttu-id="15d13-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15d13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15d13-107">*bstraupdingtext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15d13-107">*bstrPendingText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d13-108">Quelltext, der zum Generieren der Auto Vervollständigen-Liste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15d13-108">Source text to be used to generate the auto complete list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15d13-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15d13-109">Return value</span></span>

<span data-ttu-id="15d13-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="15d13-110">This method can return one of these values.</span></span>



| <span data-ttu-id="15d13-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="15d13-111">Return code</span></span>                                                                            | <span data-ttu-id="15d13-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15d13-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="15d13-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="15d13-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="15d13-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="15d13-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="15d13-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="15d13-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="15d13-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="15d13-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="15d13-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15d13-117">Remarks</span></span>

<span data-ttu-id="15d13-118">Dieser Text enthält nicht den Text, der bereits in das fokussierte Feld eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="15d13-118">This text will not contain the text already inserted in the focused field.</span></span> <span data-ttu-id="15d13-119">Der Anbieter für automatische Vervollständigung ist dafür verantwortlich, den aktuellen Feldtext und die Auswahl zum Generieren der Auto Vervollständigen-Liste zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="15d13-119">The auto complete provider is responsible for taking into account the current field text and the selection to generate the auto complete list.</span></span> <span data-ttu-id="15d13-120">Wenn *bstrautzdingtext* **null** ist, wird die Auto Vervollständigen-Liste mit dem aktuellen Text auf der linken Seite der Auswahl im Feld generiert.</span><span class="sxs-lookup"><span data-stu-id="15d13-120">When *bstrPendingText* is **NULL**, the auto complete list is generated with the current text to the left of the selection in the field.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d13-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15d13-121">Requirements</span></span>



| <span data-ttu-id="15d13-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15d13-122">Requirement</span></span> | <span data-ttu-id="15d13-123">Wert</span><span class="sxs-lookup"><span data-stu-id="15d13-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d13-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15d13-124">Minimum supported client</span></span><br/> | <span data-ttu-id="15d13-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15d13-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="15d13-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15d13-126">Minimum supported server</span></span><br/> | <span data-ttu-id="15d13-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15d13-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="15d13-128">Header</span><span class="sxs-lookup"><span data-stu-id="15d13-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="15d13-129"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="15d13-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="15d13-130">DLL</span><span class="sxs-lookup"><span data-stu-id="15d13-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15d13-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15d13-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="15d13-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15d13-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d13-133">**Itipauescompleteprovider-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="15d13-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="15d13-134">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="15d13-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




