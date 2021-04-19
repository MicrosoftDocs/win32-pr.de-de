---
description: Registriert den Anbieter beim Client, damit der Client das Auto Vervollständigen-Anbieter Objekt der Anwendung abrufen kann.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'Itipaudecompleteclient:: adviseprovider-Methode (tipaudecomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363531"
---
# <a name="itipautocompleteclientadviseprovider-method"></a><span data-ttu-id="98749-103">Itipaudecompleteclient:: adviseprovider-Methode</span><span class="sxs-lookup"><span data-stu-id="98749-103">ITipAutocompleteClient::AdviseProvider method</span></span>

<span data-ttu-id="98749-104">Registriert den Anbieter beim Client, damit der Client das Auto Vervollständigen-Anbieter Objekt der Anwendung abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="98749-104">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="98749-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98749-105">Syntax</span></span>


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="98749-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98749-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98749-107">*hwndfield* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98749-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98749-108">Das Fenster Handle des Felds, das die Funktion für automatisches Vervollständigen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="98749-108">The window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="98749-109">*piacprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98749-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98749-110">Der Schnittstellen Zeiger auf die Auto Vervollständigen-Anbieter Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="98749-110">The interface pointer to the auto complete provider interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98749-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98749-111">Return value</span></span>

<span data-ttu-id="98749-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="98749-112">This method can return one of these values.</span></span>



| <span data-ttu-id="98749-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="98749-113">Return code</span></span>                                                                            | <span data-ttu-id="98749-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98749-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="98749-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98749-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="98749-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="98749-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="98749-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="98749-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="98749-118">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="98749-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98749-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98749-119">Requirements</span></span>



| <span data-ttu-id="98749-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98749-120">Requirement</span></span> | <span data-ttu-id="98749-121">Wert</span><span class="sxs-lookup"><span data-stu-id="98749-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98749-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98749-122">Minimum supported client</span></span><br/> | <span data-ttu-id="98749-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98749-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="98749-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98749-124">Minimum supported server</span></span><br/> | <span data-ttu-id="98749-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="98749-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="98749-126">Header</span><span class="sxs-lookup"><span data-stu-id="98749-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="98749-127"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="98749-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="98749-128">DLL</span><span class="sxs-lookup"><span data-stu-id="98749-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98749-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98749-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="98749-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98749-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98749-131">**Itipauwebcompleteclient-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="98749-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="98749-132">**Itipaudecompleteclient:: unadviseprovider-Methode**</span><span class="sxs-lookup"><span data-stu-id="98749-132">**ITipAutocompleteClient::UnadviseProvider Method**</span></span>](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[<span data-ttu-id="98749-133">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="98749-133">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




