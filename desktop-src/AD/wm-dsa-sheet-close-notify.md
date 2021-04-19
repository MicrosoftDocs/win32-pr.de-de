---
title: WM_DSA_SHEET_CLOSE_NOTIFY Meldung
description: Wird an das Active Directory MMC-Snap-in gesendet, wenn ein sekundäres Eigenschaften Blatt zerstört wird.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341614"
---
# <a name="wm_dsa_sheet_close_notify-message"></a><span data-ttu-id="f0b44-104">WM- \_ DSA- \_ Blatt " \_ \_ Nachricht schließen"</span><span class="sxs-lookup"><span data-stu-id="f0b44-104">WM\_DSA\_SHEET\_CLOSE\_NOTIFY message</span></span>

<span data-ttu-id="f0b44-105">Wenn ein sekundäres Eigenschaften Blatt zerstört wird, wird die Meldung zum Schließen der Meldung zum **\_ \_ \_ Schließen \_ des WM** -MMC an das Active Directory MMC-Snap-in gesendet.</span><span class="sxs-lookup"><span data-stu-id="f0b44-105">The **WM\_DSA\_SHEET\_CLOSE\_NOTIFY** message is posted to the Active Directory MMC snap-in when a secondary property sheet is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="f0b44-106">Dieser Nachrichtenwert ist nicht in einer veröffentlichten Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="f0b44-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="f0b44-107">Wenn Sie diesen Nachrichtenwert verwenden möchten, müssen Sie ihn im exakten Format definieren.</span><span class="sxs-lookup"><span data-stu-id="f0b44-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="f0b44-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0b44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b44-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f0b44-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f0b44-110">Das Fenster Handle des Snap-in-Fensters, das diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f0b44-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="f0b44-111">Dieses Handle wird vom **hwndhidden** -Member der [**propsheetcfg**](propsheetcfg.md) -Struktur abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f0b44-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f0b44-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0b44-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0b44-113">Enthält einen von der Anwendung definierten 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="f0b44-113">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="f0b44-114">Dies wird vom **wparamsheetclose** -Member der [**propsheetcfg**](propsheetcfg.md) -Struktur abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f0b44-114">This is obtained from the **wParamSheetClose** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f0b44-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0b44-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0b44-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0b44-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b44-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0b44-117">Return value</span></span>

<span data-ttu-id="f0b44-118">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0b44-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b44-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0b44-119">Requirements</span></span>



| <span data-ttu-id="f0b44-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0b44-120">Requirement</span></span> | <span data-ttu-id="f0b44-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f0b44-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f0b44-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0b44-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b44-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0b44-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f0b44-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0b44-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b44-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0b44-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0b44-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0b44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b44-127">**Propsheetcfg**</span><span class="sxs-lookup"><span data-stu-id="f0b44-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> </dl>

 

 





