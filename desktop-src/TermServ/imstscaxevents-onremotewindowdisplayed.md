---
title: Imstscaxevents onremotewindowview-Methode
description: Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Onremotewindowview-Methode Remotedesktopdienste
- Onremotewindowview-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onremotewindowview-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392023"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a><span data-ttu-id="884de-106">Imstscaxevents:: onremotewindowview-Methode</span><span class="sxs-lookup"><span data-stu-id="884de-106">IMsTscAxEvents::OnRemoteWindowDisplayed method</span></span>

<span data-ttu-id="884de-107">Wird aufgerufen, wenn ein RemoteApp-Fenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="884de-107">Called when a RemoteApp window is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="884de-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="884de-108">Syntax</span></span>


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="884de-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="884de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="884de-110">*vbangezeigte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="884de-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884de-111">Typ: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="884de-111">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="884de-112">Gibt an, ob das RemoteApp-Fenster angezeigt oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="884de-112">Indicates whether the RemoteApp window is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="884de-113">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="884de-113">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884de-114">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="884de-114">Type: **HWND**</span></span>

<span data-ttu-id="884de-115">Das Handle des angezeigten Fensters.</span><span class="sxs-lookup"><span data-stu-id="884de-115">The handle of the window displayed.</span></span>

</dd> <dt>

<span data-ttu-id="884de-116">*windowattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="884de-116">*windowAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="884de-117">Typ: **[ **remotewindowdisplayedattribute**](remotewindowdisplayedattribute.md)**</span><span class="sxs-lookup"><span data-stu-id="884de-117">Type: **[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span></span>

<span data-ttu-id="884de-118">Ein Wert der [**remotewindowdisplayedattribute**](remotewindowdisplayedattribute.md) -Enumeration, der weitere Informationen über das Ereignis angibt.</span><span class="sxs-lookup"><span data-stu-id="884de-118">A value of the [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) enumeration that specifies more information about the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="884de-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="884de-119">Return value</span></span>

<span data-ttu-id="884de-120">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="884de-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="884de-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="884de-121">Requirements</span></span>



| <span data-ttu-id="884de-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="884de-122">Requirement</span></span> | <span data-ttu-id="884de-123">Wert</span><span class="sxs-lookup"><span data-stu-id="884de-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="884de-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="884de-124">Minimum supported client</span></span><br/> | <span data-ttu-id="884de-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="884de-125">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="884de-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="884de-126">Minimum supported server</span></span><br/> | <span data-ttu-id="884de-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="884de-127">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="884de-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="884de-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="884de-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="884de-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="884de-130">DLL</span><span class="sxs-lookup"><span data-stu-id="884de-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="884de-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="884de-131"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884de-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="884de-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884de-133">**Remotewindowdisplayedattribute**</span><span class="sxs-lookup"><span data-stu-id="884de-133">**RemoteWindowDisplayedAttribute**</span></span>](remotewindowdisplayedattribute.md)
</dt> <dt>

[<span data-ttu-id="884de-134">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="884de-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





