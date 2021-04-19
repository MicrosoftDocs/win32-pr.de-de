---
title: WM_ADSPROP_NOTIFY_APPLY Meldung (adsprop. h)
description: Eine Active Directory Verzeichnisdienst-Eigenschaften Blatt Erweiterung sendet die WM- \_ adsprop \_ Notify \_ Apply-Meldung an das Benachrichtigungs Objekt, wenn die Eigenschaften Seite "PSN \_ Apply Handler" erfolgreich ist.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345504"
---
# <a name="wm_adsprop_notify_apply-message"></a><span data-ttu-id="bde3d-104">"WM \_ adsprop \_ Notify \_ Apply Message"</span><span class="sxs-lookup"><span data-stu-id="bde3d-104">WM\_ADSPROP\_NOTIFY\_APPLY message</span></span>

<span data-ttu-id="bde3d-105">Eine Active Directory Verzeichnisdienst-Eigenschaften Blatt Erweiterung sendet die **WM- \_ adsprop \_ Notify \_ Apply** -Meldung an das Benachrichtigungs Objekt, wenn die Eigenschaften Seite "PSN \_ Apply Handler" erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bde3d-105">An Active Directory directory service property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_APPLY** message to the notification object if the property page PSN\_APPLY handler succeeds.</span></span>


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="bde3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bde3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bde3d-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bde3d-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bde3d-108">Das Handle des Benachrichtigungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="bde3d-108">The handle of the notification object.</span></span> <span data-ttu-id="bde3d-109">Rufen Sie zum Abrufen dieses Handles [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf.</span><span class="sxs-lookup"><span data-stu-id="bde3d-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="bde3d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bde3d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bde3d-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bde3d-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bde3d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bde3d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bde3d-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bde3d-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bde3d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bde3d-114">Return value</span></span>

<span data-ttu-id="bde3d-115">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="bde3d-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bde3d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bde3d-116">Remarks</span></span>

<span data-ttu-id="bde3d-117">Beim Hinzufügen von Seiten zum MMC-Snap-in "Active Directory-Manager" erstellt Active Directory MMC-Eigenschaften Blätter die Benachrichtigungsobjekte durch einen Aufrufen der Funktion " [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) " und übergibt dann das Benachrichtigungs Objekt Handle an jede Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="bde3d-117">When adding pages to the Active Directory Manager MMC snap-in, Active Directory MMC property sheets create the notification objects by a call to the [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) function, and then passes the notification object handle to each property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="bde3d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bde3d-118">Requirements</span></span>



| <span data-ttu-id="bde3d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bde3d-119">Requirement</span></span> | <span data-ttu-id="bde3d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bde3d-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bde3d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bde3d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bde3d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bde3d-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="bde3d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bde3d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bde3d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bde3d-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="bde3d-125">Header</span><span class="sxs-lookup"><span data-stu-id="bde3d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bde3d-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="bde3d-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bde3d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bde3d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde3d-128">**Adspropkreatenotifyobj**</span><span class="sxs-lookup"><span data-stu-id="bde3d-128">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="bde3d-129">Nachrichten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="bde3d-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





