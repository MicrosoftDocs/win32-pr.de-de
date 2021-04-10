---
title: WM_ADSPROP_NOTIFY_ERROR Meldung (adsprop. h)
description: Die "WM \_ adsprop \_ Notify Error"- \_ Meldung fügt eine Fehlermeldung zu einer Liste von Fehlermeldungen hinzu, die durch Aufrufen der adspropshowerrordialog-Funktion angezeigt werden.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103791"
---
# <a name="wm_adsprop_notify_error-message"></a><span data-ttu-id="788ba-104">WM \_ adsprop- \_ Benachrichtigungs \_ Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="788ba-104">WM\_ADSPROP\_NOTIFY\_ERROR message</span></span>

<span data-ttu-id="788ba-105">Die " **WM \_ adsprop \_ Notify \_ Error** "-Meldung fügt eine Fehlermeldung zu einer Liste von Fehlermeldungen hinzu, die durch Aufrufen der [**adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) -Funktion angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="788ba-105">The **WM\_ADSPROP\_NOTIFY\_ERROR** message adds an error message to a list of error messages that are displayed by calling the [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) function.</span></span>


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="788ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="788ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="788ba-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="788ba-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="788ba-108">Handle des Benachrichtigungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="788ba-108">Handle of the notification object.</span></span> <span data-ttu-id="788ba-109">Dies ist der *hnotifyobject* -Parameter, der von [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="788ba-109">This is the *hNotifyObject* parameter obtained by [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="788ba-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="788ba-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="788ba-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="788ba-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="788ba-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="788ba-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="788ba-113">Zeiger auf eine [**adsproperror**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) -Struktur, die Fehlermeldungs Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="788ba-113">Pointer to an [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) structure that contains error message data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="788ba-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="788ba-114">Return value</span></span>

<span data-ttu-id="788ba-115">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="788ba-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="788ba-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="788ba-116">Remarks</span></span>

<span data-ttu-id="788ba-117">Die [**adspropsenderrormessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) -Funktion ist die bevorzugte Methode zum Senden dieser Nachricht.</span><span class="sxs-lookup"><span data-stu-id="788ba-117">The [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) function is the preferred method of sending this message.</span></span>

<span data-ttu-id="788ba-118">Die von der " **WM \_ adsprop \_ Notify \_ Error** "-Meldung hinzugefügten Fehlermeldungen werden gesammelt, bis " [**adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="788ba-118">The error messages added by the **WM\_ADSPROP\_NOTIFY\_ERROR** message are accumulated until [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) is called.</span></span> <span data-ttu-id="788ba-119">**Adspropshowerrordialog** kombiniert die gesammelten Fehlermeldungen und zeigt diese an.</span><span class="sxs-lookup"><span data-stu-id="788ba-119">**ADsPropShowErrorDialog** combines and displays the accumulated error messages.</span></span> <span data-ttu-id="788ba-120">Wenn das Fehler Dialogfeld verworfen wird, werden die gesammelten Fehlermeldungen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="788ba-120">When the error dialog is dismissed, the accumulated error messages are deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="788ba-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="788ba-121">Requirements</span></span>



| <span data-ttu-id="788ba-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="788ba-122">Requirement</span></span> | <span data-ttu-id="788ba-123">Wert</span><span class="sxs-lookup"><span data-stu-id="788ba-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="788ba-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="788ba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="788ba-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="788ba-125">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="788ba-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="788ba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="788ba-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="788ba-127">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="788ba-128">Header</span><span class="sxs-lookup"><span data-stu-id="788ba-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="788ba-129"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="788ba-129"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="788ba-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="788ba-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788ba-131">Nachrichten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="788ba-131">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="788ba-132">**Adsproperror**</span><span class="sxs-lookup"><span data-stu-id="788ba-132">**ADSPROPERROR**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[<span data-ttu-id="788ba-133">**Adspropsenderrormessage**</span><span class="sxs-lookup"><span data-stu-id="788ba-133">**ADsPropSendErrorMessage**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[<span data-ttu-id="788ba-134">**Adspropshowerrordialog**</span><span class="sxs-lookup"><span data-stu-id="788ba-134">**ADsPropShowErrorDialog**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





