---
description: Benachrichtigt den Eingabebereich, dass der Benutzer etwas in der Liste Auto vervollständigen ausgewählt und den verbleibenden Text verworfen hat, der noch nicht eingefügt wurde.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'Itipaudecompleteclient:: userselection-Methode (tipaudecomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351735"
---
# <a name="itipautocompleteclientuserselection-method"></a><span data-ttu-id="37f44-103">Itipaudecompleteclient:: userselection-Methode</span><span class="sxs-lookup"><span data-stu-id="37f44-103">ITipAutocompleteClient::UserSelection method</span></span>

<span data-ttu-id="37f44-104">Benachrichtigt den Eingabebereich, dass der Benutzer etwas in der Liste Auto vervollständigen ausgewählt und den verbleibenden Text verworfen hat, der noch nicht eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="37f44-104">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f44-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37f44-105">Syntax</span></span>


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a><span data-ttu-id="37f44-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37f44-106">Parameters</span></span>

<span data-ttu-id="37f44-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="37f44-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37f44-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37f44-108">Return value</span></span>

<span data-ttu-id="37f44-109">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="37f44-109">This method can return one of these values.</span></span>



| <span data-ttu-id="37f44-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="37f44-110">Return code</span></span>                                                                            | <span data-ttu-id="37f44-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37f44-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="37f44-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="37f44-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="37f44-113">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="37f44-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="37f44-114"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="37f44-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="37f44-115">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37f44-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37f44-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37f44-116">Remarks</span></span>

<span data-ttu-id="37f44-117">Diese Methode wird vom Anbieter aufgerufen, um den Client zu benachrichtigen, dass der Benutzer eine Auswahl getroffen hat.</span><span class="sxs-lookup"><span data-stu-id="37f44-117">This method is called from the provider to notify the client that a selection has been made by the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="37f44-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37f44-118">Requirements</span></span>



| <span data-ttu-id="37f44-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37f44-119">Requirement</span></span> | <span data-ttu-id="37f44-120">Wert</span><span class="sxs-lookup"><span data-stu-id="37f44-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f44-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37f44-121">Minimum supported client</span></span><br/> | <span data-ttu-id="37f44-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37f44-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="37f44-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37f44-123">Minimum supported server</span></span><br/> | <span data-ttu-id="37f44-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="37f44-124">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="37f44-125">Header</span><span class="sxs-lookup"><span data-stu-id="37f44-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f44-126"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="37f44-126"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="37f44-127">DLL</span><span class="sxs-lookup"><span data-stu-id="37f44-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37f44-128"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37f44-128"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="37f44-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37f44-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f44-130">**Itipauwebcompleteclient-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="37f44-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="37f44-131">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="37f44-131">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




