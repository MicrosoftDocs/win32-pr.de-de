---
description: Bestimmt, ob der Eingabebereich bereit ist, die Auto Vervollständigen-Liste angezeigt zu haben.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'Itipautocompleteclient:: requestshowui-Methode (tipautocomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216407"
---
# <a name="itipautocompleteclientrequestshowui-method"></a><span data-ttu-id="d233c-103">Itipautocompleteclient:: requestshowui-Methode</span><span class="sxs-lookup"><span data-stu-id="d233c-103">ITipAutocompleteClient::RequestShowUI method</span></span>

<span data-ttu-id="d233c-104">Bestimmt, ob der Eingabebereich bereit ist, die Auto Vervollständigen-Liste angezeigt zu haben.</span><span class="sxs-lookup"><span data-stu-id="d233c-104">Determines whether Input Panel is ready to have the auto complete list shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="d233c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d233c-105">Syntax</span></span>


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a><span data-ttu-id="d233c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d233c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d233c-107">*hwndaclist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d233c-107">*hWndACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d233c-108">Fenster Handle der Benutzeroberfläche für die automatische Vervollständigung.</span><span class="sxs-lookup"><span data-stu-id="d233c-108">Window handle of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="d233c-109">*pfallow-Anzeige* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d233c-109">*pfAllowShowing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d233c-110">**False** , wenn vom Client empfohlen wird, die Benutzeroberfläche für die automatische Vervollständigung nicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d233c-110">**FALSE** if client recommends to not show the auto complete list user interface.</span></span> <span data-ttu-id="d233c-111">**True** , wenn der Anbieter für automatische Vervollständigung die Listen Benutzeroberfläche anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="d233c-111">**TRUE** if the auto complete provider can show the list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d233c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d233c-112">Return value</span></span>

<span data-ttu-id="d233c-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d233c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="d233c-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d233c-114">Return code</span></span>                                                                            | <span data-ttu-id="d233c-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d233c-115">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d233c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d233c-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d233c-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="d233c-117">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d233c-118"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="d233c-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d233c-119">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d233c-119">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d233c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d233c-120">Remarks</span></span>

<span data-ttu-id="d233c-121">Diese Methode wird vom Auto Vervollständigen-Anbieter aufgerufen, wenn die Benutzeroberfläche für die automatische Vervollständigung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d233c-121">This method is called by the auto complete provider when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="d233c-122">Wenn der interne Zustand des Clients die Benutzeroberfläche nicht anzeigen kann, wird *pfallowshow* auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d233c-122">If the client's internal state doesn't allow the provider to show the user interface, *pfAllowShowing* will be set to **FALSE**.</span></span> <span data-ttu-id="d233c-123">Wenn der Text z. b. aus dem Handschrift Design des Tablet PC-Eingabe Bereichs an das Feld gesendet wird und der Benutzer sofort mit dem Binden beginnt, wird empfohlen, die Benutzeroberfläche für die automatische Vervollständigung nicht anzuzeigen, um zu vermeiden, dass das Inking des Benutzers zerstört wird, indem *pfallowshow* auf **false** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d233c-123">For example, when the text gets sent to the field from the handwriting skin on the Tablet PC Input Panel and the user immediately starts inking, the client will recommend to not show the auto complete user interface, in order to avoid destructing the user's inking, by setting *pfAllowShowing* to **FALSE**.</span></span>

<span data-ttu-id="d233c-124">Aufrufen von **requestshowui** , um das Fenster Handle für das automatische Popup-Listenfenster festzulegen, bevor Sie die [**itipautocompleteclient::P referredrects-Methode**](itipautocompleteclient-preferredrects.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d233c-124">Call **RequestShowUI** to set the popup auto complete list window handle before you call the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span> <span data-ttu-id="d233c-125">Wenn dies nicht der Fall ist, wird beim Aufrufen von " **preferredrects**" ein **E \_ invalidArg** -Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d233c-125">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d233c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d233c-126">Requirements</span></span>



| <span data-ttu-id="d233c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d233c-127">Requirement</span></span> | <span data-ttu-id="d233c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d233c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d233c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d233c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d233c-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d233c-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="d233c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d233c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d233c-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d233c-132">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="d233c-133">Header</span><span class="sxs-lookup"><span data-stu-id="d233c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d233c-134"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="d233c-134"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d233c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d233c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d233c-136"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d233c-136"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="d233c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d233c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d233c-138">**Itipauwebcompleteclient-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d233c-138">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="d233c-139">**Itipaudecompleteclient::P referredrects-Methode**</span><span class="sxs-lookup"><span data-stu-id="d233c-139">**ITipAutocompleteClient::PreferredRects Method**</span></span>](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[<span data-ttu-id="d233c-140">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="d233c-140">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




