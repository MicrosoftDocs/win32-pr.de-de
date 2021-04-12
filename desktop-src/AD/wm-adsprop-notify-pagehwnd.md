---
title: WM_ADSPROP_NOTIFY_PAGEHWND Meldung (adsprop. h)
description: Eine Active Directory Verzeichnisdienst-Eigenschaften Blatt Erweiterung ruft das adspropsethwnd auf, um das Benachrichtigungs Objekt des Fenster Handles der Eigenschaften Seite zu informieren.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEHWND Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105615"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a><span data-ttu-id="6852f-104">"WM \_ adsprop"- \_ Benachrichtigungs \_ Meldung Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="6852f-104">WM\_ADSPROP\_NOTIFY\_PAGEHWND message</span></span>

<span data-ttu-id="6852f-105">Eine Active Directory Verzeichnisdienst-Eigenschaften Blatt Erweiterung ruft das [**adspropsethwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) auf, um das Benachrichtigungs Objekt des Fenster Handles der Eigenschaften Seite zu informieren.</span><span class="sxs-lookup"><span data-stu-id="6852f-105">An Active Directory directory service property sheet extension calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) to inform the notification object of the property page window handle.</span></span> <span data-ttu-id="6852f-106">Die **adspropsethwnd** -Funktion sendet die " **WM \_ adsprop \_ Notify \_ pagehwnd** "-Nachricht an das Benachrichtigungs Objekt, das das Benachrichtigungs Objekt des Fenster Handles der Eigenschaften Seite informiert.</span><span class="sxs-lookup"><span data-stu-id="6852f-106">The **ADsPropSetHwnd** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEHWND** message to the notification object, which informs the notification object of the property page window handle.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a><span data-ttu-id="6852f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6852f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6852f-108">*hnotifyobj*</span><span class="sxs-lookup"><span data-stu-id="6852f-108">*hNotifyObj*</span></span> 
</dt> <dd>

<span data-ttu-id="6852f-109">Das Handle des Benachrichtigungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="6852f-109">The handle of the notification object.</span></span> <span data-ttu-id="6852f-110">Rufen Sie zum Abrufen dieses Handles [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf.</span><span class="sxs-lookup"><span data-stu-id="6852f-110">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="6852f-111">*hPage*</span><span class="sxs-lookup"><span data-stu-id="6852f-111">*hPage*</span></span> 
</dt> <dd>

<span data-ttu-id="6852f-112">Ein Fenster Handle der Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="6852f-112">A window handle of the property page.</span></span>

</dd> <dt>

<span data-ttu-id="6852f-113">*ptztitle*</span><span class="sxs-lookup"><span data-stu-id="6852f-113">*ptzTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="6852f-114">Ein Zeiger auf einen null-terminierten **WCHAR** -Puffer, der den Titel der Eigenschaften Seite enthält.</span><span class="sxs-lookup"><span data-stu-id="6852f-114">Pointer to a NULL-terminated **WCHAR** buffer that contains the title of the property page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6852f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6852f-115">Return value</span></span>

<span data-ttu-id="6852f-116">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="6852f-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6852f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6852f-117">Remarks</span></span>

<span data-ttu-id="6852f-118">Eine Active Directory Eigenschaften Blatt Erweiterung ruft bei der Verarbeitung der [**WM- \_ InitDialog**](../dlgbox/wm-initdialog.md) -Nachricht normalerweise die Funktion [**adspropabthwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) auf.</span><span class="sxs-lookup"><span data-stu-id="6852f-118">An Active Directory property sheet extension normally calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) function while processing the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6852f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6852f-119">Requirements</span></span>



| <span data-ttu-id="6852f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6852f-120">Requirement</span></span> | <span data-ttu-id="6852f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6852f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6852f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6852f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6852f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6852f-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="6852f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6852f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6852f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6852f-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="6852f-126">Header</span><span class="sxs-lookup"><span data-stu-id="6852f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6852f-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="6852f-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6852f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6852f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6852f-129">Nachrichten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6852f-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="6852f-130">**Adspropsetup**</span><span class="sxs-lookup"><span data-stu-id="6852f-130">**ADsPropSetHwnd**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[<span data-ttu-id="6852f-131">**Adspropkreatenotifyobj**</span><span class="sxs-lookup"><span data-stu-id="6852f-131">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="6852f-132">**WM \_ InitDialog**</span><span class="sxs-lookup"><span data-stu-id="6852f-132">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

