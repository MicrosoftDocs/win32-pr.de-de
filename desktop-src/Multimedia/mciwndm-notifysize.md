---
title: MCIWNDM_NOTIFYSIZE Meldung (VFW. h)
description: Die Meldung mciwndm \_ notifiysize benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fenstergröße geändert hat.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103434"
---
# <a name="mciwndm_notifysize-message"></a><span data-ttu-id="112be-104">Meldung zu mciwndm \_ notifiysize</span><span class="sxs-lookup"><span data-stu-id="112be-104">MCIWNDM\_NOTIFYSIZE message</span></span>

<span data-ttu-id="112be-105">Die Meldung **mciwndm \_ notifiysize** benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fenstergröße geändert hat.</span><span class="sxs-lookup"><span data-stu-id="112be-105">The **MCIWNDM\_NOTIFYSIZE** message notifies the parent window of an application that the window size has changed.</span></span>


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="112be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="112be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="112be-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="112be-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="112be-108">Handle für das mciwnd-Fenster.</span><span class="sxs-lookup"><span data-stu-id="112be-108">Handle to the MCIWnd window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="112be-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="112be-109">Remarks</span></span>

<span data-ttu-id="112be-110">Sie können die Benachrichtigung über Änderungen in der Größe eines mciwnd-Fensters aktivieren, indem Sie den mciwndf- \_ Fenster Stil "notifysize" angeben.</span><span class="sxs-lookup"><span data-stu-id="112be-110">You can enable notification of changes in the size of an MCIWnd window by specifying the MCIWNDF\_NOTIFYSIZE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="112be-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="112be-111">Requirements</span></span>



| <span data-ttu-id="112be-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="112be-112">Requirement</span></span> | <span data-ttu-id="112be-113">Wert</span><span class="sxs-lookup"><span data-stu-id="112be-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="112be-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="112be-114">Minimum supported client</span></span><br/> | <span data-ttu-id="112be-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="112be-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="112be-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="112be-116">Minimum supported server</span></span><br/> | <span data-ttu-id="112be-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="112be-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="112be-118">Header</span><span class="sxs-lookup"><span data-stu-id="112be-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="112be-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="112be-119"><dt>Vfw.h</dt></span></span> </dl> |



 

 





