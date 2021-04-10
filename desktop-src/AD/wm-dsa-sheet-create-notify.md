---
title: WM_DSA_SHEET_CREATE_NOTIFY Meldung
description: Wird im Active Directory MMC-Snap-in zum Erstellen eines sekundären Eigenschaften Blatts gepostet.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956546"
---
# <a name="wm_dsa_sheet_create_notify-message"></a><span data-ttu-id="a32bb-104">WM- \_ DSA- \_ Blatt " \_ \_ Nachricht benachrichtigen" erstellen</span><span class="sxs-lookup"><span data-stu-id="a32bb-104">WM\_DSA\_SHEET\_CREATE\_NOTIFY message</span></span>

<span data-ttu-id="a32bb-105">Das **WM- \_ DSA- \_ Blatt \_ Create \_ Notify** Message wird im Active Directory MMC-Snap-in zum Erstellen eines sekundären Eigenschaften Blatts gepostet.</span><span class="sxs-lookup"><span data-stu-id="a32bb-105">The **WM\_DSA\_SHEET\_CREATE\_NOTIFY** message is posted to the Active Directory MMC snap-in to create a secondary property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="a32bb-106">Dieser Nachrichtenwert ist nicht in einer veröffentlichten Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="a32bb-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="a32bb-107">Um diesen Nachrichtenwert zu verwenden, definieren Sie ihn im exakten Format.</span><span class="sxs-lookup"><span data-stu-id="a32bb-107">To use this message value, define it in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="a32bb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a32bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a32bb-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a32bb-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a32bb-110">Das Fenster Handle des Snap-in-Fensters, das diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a32bb-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="a32bb-111">Dieses Handle wird vom **hwndhidden** -Member der [**propsheetcfg**](propsheetcfg.md) -Struktur abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a32bb-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a32bb-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a32bb-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a32bb-113">Enthält einen Zeiger auf eine [**DSA \_ sec- \_ Seiten \_ Informations**](dsa-sec-page-info.md) Struktur, die das zu Erstell führende sekundäre Eigenschaften Blatt definiert.</span><span class="sxs-lookup"><span data-stu-id="a32bb-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary property sheet to create.</span></span> <span data-ttu-id="a32bb-114">Der Nachrichtenempfänger muss diesen Arbeitsspeicher mit der [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) -Funktion freigeben, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a32bb-114">The message receiver must free this memory with the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function when it is no longer required.</span></span>

</dd> <dt>

<span data-ttu-id="a32bb-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a32bb-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a32bb-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a32bb-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a32bb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a32bb-117">Return value</span></span>

<span data-ttu-id="a32bb-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a32bb-118">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32bb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a32bb-119">Requirements</span></span>



| <span data-ttu-id="a32bb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a32bb-120">Requirement</span></span> | <span data-ttu-id="a32bb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a32bb-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a32bb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a32bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a32bb-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a32bb-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a32bb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a32bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a32bb-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a32bb-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a32bb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a32bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a32bb-127">**Propsheetcfg**</span><span class="sxs-lookup"><span data-stu-id="a32bb-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> <dt>

[<span data-ttu-id="a32bb-128">**\_ \_ Seite \_ Informationen zu DSA sec**</span><span class="sxs-lookup"><span data-stu-id="a32bb-128">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="a32bb-129">**Von LocalFree**</span><span class="sxs-lookup"><span data-stu-id="a32bb-129">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

