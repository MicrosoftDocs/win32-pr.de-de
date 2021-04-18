---
description: Ermöglicht dem Client, vorzuschlagen, wo die Auto Vervollständigen-Liste positioniert werden soll, um die überlappenden Eingabebereich zu vermeiden.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: Itipaudecompleteclient::P referredrects-Methode (tipaudecomplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347725"
---
# <a name="itipautocompleteclientpreferredrects-method"></a><span data-ttu-id="ef921-103">Itipaudecompleteclient::P referredrects-Methode</span><span class="sxs-lookup"><span data-stu-id="ef921-103">ITipAutocompleteClient::PreferredRects method</span></span>

<span data-ttu-id="ef921-104">Ermöglicht dem Client, vorzuschlagen, wo die Auto Vervollständigen-Liste positioniert werden soll, um die überlappenden Eingabebereich zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ef921-104">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef921-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef921-105">Syntax</span></span>


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a><span data-ttu-id="ef921-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef921-107">*prcaclist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef921-107">*prcACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef921-108">Ein Rechteck in Bildschirm Koordinaten, das den bevorzugten Speicherort des Anbieters und die Größe der Benutzeroberfläche für die automatische vollständige Liste angibt.</span><span class="sxs-lookup"><span data-stu-id="ef921-108">A rectangle, in screen coordinates, indicating the provider's preferred location and the size of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="ef921-109">*prcfield* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef921-109">*prcField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef921-110">Ein Rechteck in Bildschirm Koordinaten, das die Position und die Größe des Fokus Felds angibt.</span><span class="sxs-lookup"><span data-stu-id="ef921-110">A rectangle, in screen coordinates, indicating the location and the size of the focused field.</span></span>

</dd> <dt>

<span data-ttu-id="ef921-111">*prcmodified* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ef921-111">*prcModified* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef921-112">Ein Rechteck, das auf dem aktuellen Status des Tipps und dem bevorzugten, durch *prcaclist* angegebenen Speicherort für die automatische Vervollständigung und Größe basiert.</span><span class="sxs-lookup"><span data-stu-id="ef921-112">A rectangle based on the current state of the TIP and the preferred auto complete list location and size specified by *prcACList*.</span></span>

</dd> <dt>

<span data-ttu-id="ef921-113">*pfshownabovetip* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ef921-113">*pfShownAboveTip* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef921-114">**True** , wenn das geänderte Rechteck über dem Zielbereich des Text Eintrags angezeigt werden soll. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ef921-114">**TRUE** if the modified rectangle is to be shown above the Text Input Panel's target area; otherwise, **FALSE**.</span></span> <span data-ttu-id="ef921-115">Dieser Wert muss mit der bevorzugten Ausrichtung des Anbieters initialisiert werden, bevor die-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ef921-115">This value must be initialized to the provider's preferred orientation before the method is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef921-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef921-116">Return value</span></span>

<span data-ttu-id="ef921-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ef921-117">This method can return one of these values.</span></span>



| <span data-ttu-id="ef921-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef921-118">Return code</span></span>                                                                                  | <span data-ttu-id="ef921-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef921-119">Description</span></span>                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef921-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef921-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ef921-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ef921-121">Success.</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="ef921-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ef921-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ef921-123">Rufen Sie die [**itipautocompleteclient:: requestshowui-Methode**](itipautocompleteclient-requestshowui.md) auf, um das Popup Fenster für das automatische vollständige Popup Fenster vor dem Aufrufen der [**itipautocompleteclient::P referredrects-Methode**](itipautocompleteclient-preferredrects.md)festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ef921-123">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window before calling the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span><br/> |
| <dl> <span data-ttu-id="ef921-124"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="ef921-124"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="ef921-125">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ef921-125">An unspecified error occurred.</span></span><br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="ef921-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef921-126">Remarks</span></span>

<span data-ttu-id="ef921-127">Dies ist die Methode, die der Auto Vervollständigen-Anbieter aufruft, wenn die automatische Vervollständigung der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ef921-127">This is the method that the auto complete provider calls when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="ef921-128">Der Client ändert das bevorzugte Rechteck des Anbieters, das durch *prcaclist* über das *prcmodified* -Argument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef921-128">The client modifies the provider's preferred rectangle specified by *prcACList* through *prcModified* argument.</span></span>

<span data-ttu-id="ef921-129">Aufrufen der [**itipautocompleteclient:: requestshowui-Methode**](itipautocompleteclient-requestshowui.md) , um das Fenster Handle für die automatische Vervollständigung des Popups vor dem Aufrufen von **preferredrects** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ef921-129">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window handle before you call **PreferredRects**.</span></span> <span data-ttu-id="ef921-130">Wenn dies nicht der Fall ist, wird beim Aufrufen von " **preferredrects**" ein **E \_ invalidArg** -Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef921-130">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef921-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef921-131">Requirements</span></span>



| <span data-ttu-id="ef921-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef921-132">Requirement</span></span> | <span data-ttu-id="ef921-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ef921-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef921-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef921-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ef921-135">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef921-135">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ef921-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef921-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ef921-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ef921-137">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="ef921-138">Header</span><span class="sxs-lookup"><span data-stu-id="ef921-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef921-139"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="ef921-139"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ef921-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ef921-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef921-141"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef921-141"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="ef921-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef921-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef921-143">**Itipauwebcompleteclient-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ef921-143">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="ef921-144">**Itipautocompleteclient:: requestshowui-Methode**</span><span class="sxs-lookup"><span data-stu-id="ef921-144">**ITipAutocompleteClient::RequestShowUI Method**</span></span>](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[<span data-ttu-id="ef921-145">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="ef921-145">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




