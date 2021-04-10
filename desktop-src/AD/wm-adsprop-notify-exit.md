---
title: WM_ADSPROP_NOTIFY_EXIT Meldung (adsprop. h)
description: Eine Active Directory-Eigenschafts Blatt Erweiterung sendet die WM-Benachrichtigung zum \_ \_ Benachrichtigen der \_ Nachricht an das Benachrichtigungs Objekt, wenn das Benachrichtigungs Objekt nicht mehr benötigt wird.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_EXIT Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957012"
---
# <a name="wm_adsprop_notify_exit-message"></a><span data-ttu-id="fad42-104">WM \_ adsprop \_ Notify \_ Exit Message</span><span class="sxs-lookup"><span data-stu-id="fad42-104">WM\_ADSPROP\_NOTIFY\_EXIT message</span></span>

<span data-ttu-id="fad42-105">Eine Active Directory-Eigenschafts Blatt Erweiterung sendet die WM-Benachrichtigung zum **\_ \_ Benachrichtigen \_** der Nachricht an das Benachrichtigungs Objekt, wenn das Benachrichtigungs Objekt nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="fad42-105">An Active Directory property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_EXIT** message to the notification object when the notification object is no longer required.</span></span>


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="fad42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fad42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad42-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="fad42-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fad42-108">Das Handle des Benachrichtigungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="fad42-108">The handle of the notification object.</span></span> <span data-ttu-id="fad42-109">Rufen Sie zum Abrufen dieses Handles [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf.</span><span class="sxs-lookup"><span data-stu-id="fad42-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="fad42-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fad42-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fad42-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fad42-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fad42-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fad42-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fad42-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fad42-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad42-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fad42-114">Return value</span></span>

<span data-ttu-id="fad42-115">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="fad42-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad42-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fad42-116">Remarks</span></span>

<span data-ttu-id="fad42-117">Das Benachrichtigungs Objekt wird als Antwort auf diese Nachricht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fad42-117">The notification object will delete itself in response to this message.</span></span> <span data-ttu-id="fad42-118">Wenn diese Nachricht gesendet wurde, sollte das Benachrichtigungs Objekt Handle als ungültig betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="fad42-118">When this message has been sent, the notification object handle should be considered invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad42-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fad42-119">Requirements</span></span>



| <span data-ttu-id="fad42-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fad42-120">Requirement</span></span> | <span data-ttu-id="fad42-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fad42-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fad42-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fad42-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fad42-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fad42-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="fad42-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fad42-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fad42-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fad42-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="fad42-126">Header</span><span class="sxs-lookup"><span data-stu-id="fad42-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fad42-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad42-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad42-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fad42-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad42-129">**Adspropkreatenotifyobj**</span><span class="sxs-lookup"><span data-stu-id="fad42-129">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="fad42-130">Nachrichten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="fad42-130">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





