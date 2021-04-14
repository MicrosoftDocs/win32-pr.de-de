---
title: WM_ADSPROP_SHEET_CREATE Meldung
description: Wird an das Benachrichtigungs Objekt gesendet, um ein sekundäres Eigenschaften Blatt in einem Active Directory MMC-Snap-in zu erstellen.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_SHEET_CREATE Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517837"
---
# <a name="wm_adsprop_sheet_create-message"></a><span data-ttu-id="da22c-104">Meldung zum Erstellen eines "WM \_ adsprop"- \_ Blatts \_</span><span class="sxs-lookup"><span data-stu-id="da22c-104">WM\_ADSPROP\_SHEET\_CREATE message</span></span>

<span data-ttu-id="da22c-105">Die Meldung " **WM \_ adsprop \_ Sheet \_ Create** " wird an das Benachrichtigungs Objekt gesendet, um ein sekundäres Eigenschaften Blatt in einem Active Directory MMC-Snap-in zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da22c-105">The **WM\_ADSPROP\_SHEET\_CREATE** message is sent to the notification object to create a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="da22c-106">Dieser Nachrichtenwert ist nicht in einer veröffentlichten Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="da22c-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="da22c-107">Wenn Sie diesen Nachrichtenwert verwenden möchten, müssen Sie ihn im exakten Format definieren.</span><span class="sxs-lookup"><span data-stu-id="da22c-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="da22c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="da22c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da22c-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="da22c-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="da22c-110">Das Handle des Benachrichtigungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="da22c-110">The handle of the notification object.</span></span> <span data-ttu-id="da22c-111">Rufen Sie zum Abrufen dieses Handles [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)auf.</span><span class="sxs-lookup"><span data-stu-id="da22c-111">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="da22c-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da22c-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da22c-113">Enthält einen Zeiger auf eine [**DSA \_ sec- \_ Seiten \_ Informations**](dsa-sec-page-info.md) Struktur, die die zu Erstell führende sekundäre Seite definiert.</span><span class="sxs-lookup"><span data-stu-id="da22c-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary page to create.</span></span> <span data-ttu-id="da22c-114">Es kann nur ein sekundäres Eigenschaften Blatt mit der Meldung " **WM \_ adsprop \_ Sheet \_ Create** " erstellt werden, sodass die [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur nur eine [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Struktur enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="da22c-114">Only one secondary property sheet can be created with the **WM\_ADSPROP\_SHEET\_CREATE** message, so the [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da22c-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da22c-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da22c-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="da22c-116">Not used.</span></span> <span data-ttu-id="da22c-117">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="da22c-117">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da22c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da22c-118">Return value</span></span>

<span data-ttu-id="da22c-119">Der Rückgabewert für diese Nachricht ist immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="da22c-119">The return value for this message is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="da22c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da22c-120">Remarks</span></span>

<span data-ttu-id="da22c-121">Der Aufrufer muss die [**DSA \_ sec- \_ Seiten \_ Informations**](dsa-sec-page-info.md) Struktur, die Titel Zeichenfolge und alle [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Zeichen folgen mit einem einzigen Aufruf der [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) -Funktion zuordnen.</span><span class="sxs-lookup"><span data-stu-id="da22c-121">The caller must allocate the [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure, the title string and all [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) strings using a single call to the [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) function.</span></span> <span data-ttu-id="da22c-122">Die Meldung " **WM \_ adsprop \_ Sheet \_ Create** " ist eine asynchrone Nachricht und wird daher vor der Erstellung des sekundären Blatts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da22c-122">The **WM\_ADSPROP\_SHEET\_CREATE** message is an asynchronous message, so it will return before the secondary sheet is created.</span></span> <span data-ttu-id="da22c-123">Aus diesem Grund muss der Arbeitsspeicher beibehalten werden, nachdem die Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="da22c-123">Because of this, the memory must remain intact after the message returns.</span></span> <span data-ttu-id="da22c-124">Der Empfänger gibt diesen Arbeitsspeicher mit einem einzigen-Befehl der [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) -Funktion frei, nachdem das sekundäre Blatt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="da22c-124">The receiver will free this memory with a single call to the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function after the secondary sheet is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="da22c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da22c-125">Requirements</span></span>



| <span data-ttu-id="da22c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da22c-126">Requirement</span></span> | <span data-ttu-id="da22c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="da22c-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="da22c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da22c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="da22c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da22c-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="da22c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da22c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="da22c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da22c-131">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da22c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da22c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da22c-133">**cfstr \_ DS- \_ Klammern**</span><span class="sxs-lookup"><span data-stu-id="da22c-133">**CFSTR\_DS\_PARENTHWND**</span></span>](cfstr-ds-parenthwnd.md)
</dt> <dt>

[<span data-ttu-id="da22c-134">**\_ \_ Seite \_ Informationen zu DSA sec**</span><span class="sxs-lookup"><span data-stu-id="da22c-134">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="da22c-135">**Dsobjectnames**</span><span class="sxs-lookup"><span data-stu-id="da22c-135">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="da22c-136">**Dsobject**</span><span class="sxs-lookup"><span data-stu-id="da22c-136">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[<span data-ttu-id="da22c-137">**Localzuweisung**</span><span class="sxs-lookup"><span data-stu-id="da22c-137">**LocalAlloc**</span></span>](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[<span data-ttu-id="da22c-138">**Von LocalFree**</span><span class="sxs-lookup"><span data-stu-id="da22c-138">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

