---
description: Fordert den Titel und den Text für ein Chevron-Infotipp für das von der zugehörigen smdata-Struktur angegebene Element an.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: SMC_CHEVRONGETTIP Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980176"
---
# <a name="smc_chevrongettip-message"></a><span data-ttu-id="9d247-103">SMC \_ chevrongettip-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9d247-103">SMC\_CHEVRONGETTIP message</span></span>

<span data-ttu-id="9d247-104">Fordert den Titel und den Text für ein Chevron-Infotipp für das von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebene Element an.</span><span class="sxs-lookup"><span data-stu-id="9d247-104">Requests the title and text for a chevron infotip for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a><span data-ttu-id="9d247-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d247-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d247-106">*pwsztiptitle*</span><span class="sxs-lookup"><span data-stu-id="9d247-106">*pwszTipTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="9d247-107">Ein Zeiger auf einen Puffer, der eine **null**-terminierte Unicode-Zeichenfolge mit dem Titel des infotip empfängt.</span><span class="sxs-lookup"><span data-stu-id="9d247-107">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's title.</span></span> <span data-ttu-id="9d247-108">Diese Zeichenfolge darf nicht länger sein als \_ die maximale Länge von Pfad Zeichen, einschließlich des abschließenden **null** -Zeichens.</span><span class="sxs-lookup"><span data-stu-id="9d247-108">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="9d247-109">*pwsztiptext*</span><span class="sxs-lookup"><span data-stu-id="9d247-109">*pwszTipText*</span></span> 
</dt> <dd>

<span data-ttu-id="9d247-110">Ein Zeiger auf einen Puffer, der eine **null**-terminierte Unicode-Zeichenfolge empfängt, die den Text des infotip enthält.</span><span class="sxs-lookup"><span data-stu-id="9d247-110">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's text.</span></span> <span data-ttu-id="9d247-111">Diese Zeichenfolge darf nicht länger sein als \_ die maximale Länge von Pfad Zeichen, einschließlich des abschließenden **null** -Zeichens.</span><span class="sxs-lookup"><span data-stu-id="9d247-111">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d247-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d247-112">Return value</span></span>

<span data-ttu-id="9d247-113">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="9d247-113">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d247-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d247-114">Remarks</span></span>

<span data-ttu-id="9d247-115">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="9d247-115">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d247-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9d247-116">Requirements</span></span>



| <span data-ttu-id="9d247-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d247-117">Requirement</span></span> | <span data-ttu-id="9d247-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9d247-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d247-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d247-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9d247-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d247-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d247-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d247-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9d247-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d247-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d247-123">Header</span><span class="sxs-lookup"><span data-stu-id="9d247-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d247-124"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d247-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d247-125">IDL</span><span class="sxs-lookup"><span data-stu-id="9d247-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d247-126"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d247-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




