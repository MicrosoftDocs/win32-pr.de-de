---
description: Hebt die Registrierung des zugeordneten Anbieters auf.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'Itipaudecompleteclient:: unadviseprovider-Methode (tipaudecomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865820"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a><span data-ttu-id="e44ed-103">Itipaudecompleteclient:: unadviseprovider-Methode</span><span class="sxs-lookup"><span data-stu-id="e44ed-103">ITipAutocompleteClient::UnadviseProvider method</span></span>

<span data-ttu-id="e44ed-104">Hebt die Registrierung des zugeordneten Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="e44ed-104">Unregisters the associated provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e44ed-105">Syntax</span></span>


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="e44ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e44ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e44ed-107">*hwndfield* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e44ed-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44ed-108">Fenster Handle des Felds, das die Funktion für automatisches Vervollständigen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e44ed-108">Window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="e44ed-109">*piacprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e44ed-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44ed-110">Der Schnittstellen Zeiger auf die Auto Vervollständigen-Anbieter Schnittstelle, deren Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e44ed-110">Interface pointer to the auto complete provider interface to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e44ed-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e44ed-111">Return value</span></span>

<span data-ttu-id="e44ed-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e44ed-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e44ed-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e44ed-113">Return code</span></span>                                                                            | <span data-ttu-id="e44ed-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e44ed-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e44ed-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e44ed-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e44ed-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e44ed-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e44ed-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="e44ed-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e44ed-118">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e44ed-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e44ed-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e44ed-119">Requirements</span></span>



| <span data-ttu-id="e44ed-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e44ed-120">Requirement</span></span> | <span data-ttu-id="e44ed-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e44ed-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e44ed-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e44ed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e44ed-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e44ed-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="e44ed-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e44ed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e44ed-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e44ed-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="e44ed-126">Header</span><span class="sxs-lookup"><span data-stu-id="e44ed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e44ed-127"><dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt></span><span class="sxs-lookup"><span data-stu-id="e44ed-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e44ed-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e44ed-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e44ed-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e44ed-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="e44ed-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e44ed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e44ed-131">**Itipauwebcompleteclient-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e44ed-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="e44ed-132">Verweis auf Text Eingabe Panel</span><span class="sxs-lookup"><span data-stu-id="e44ed-132">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




