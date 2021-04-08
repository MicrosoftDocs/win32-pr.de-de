---
title: MCIWNDM_NOTIFYPOS Meldung (VFW. h)
description: Die mciwndm \_ notifypos-Nachricht benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fensterposition geändert hat.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956970"
---
# <a name="mciwndm_notifypos-message"></a><span data-ttu-id="57da0-104">Mciwndm \_ notifypos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="57da0-104">MCIWNDM\_NOTIFYPOS message</span></span>

<span data-ttu-id="57da0-105">Die **mciwndm \_ notifypos** -Nachricht benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fensterposition geändert hat.</span><span class="sxs-lookup"><span data-stu-id="57da0-105">The **MCIWNDM\_NOTIFYPOS** message notifies the parent window of an application that the window position has changed.</span></span>


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a><span data-ttu-id="57da0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57da0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57da0-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="57da0-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="57da0-108">Handle für das mciwnd-Fenster.</span><span class="sxs-lookup"><span data-stu-id="57da0-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="57da0-109"><span id="pos"></span><span id="POS"></span>*POS*</span><span class="sxs-lookup"><span data-stu-id="57da0-109"><span id="pos"></span><span id="POS"></span>*pos*</span></span>
</dt> <dd>

<span data-ttu-id="57da0-110">Beschreibt die neue Position.</span><span class="sxs-lookup"><span data-stu-id="57da0-110">Describes the new position.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57da0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57da0-111">Remarks</span></span>

<span data-ttu-id="57da0-112">Sie können die Benachrichtigung über Änderungen an der Position eines mciwnd-Fensters aktivieren, indem Sie den Fenster Stil mciwndf \_ notifypos angeben.</span><span class="sxs-lookup"><span data-stu-id="57da0-112">You can enable notification of changes in the position of an MCIWnd window by specifying the MCIWNDF\_NOTIFYPOS window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="57da0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57da0-113">Requirements</span></span>



| <span data-ttu-id="57da0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57da0-114">Requirement</span></span> | <span data-ttu-id="57da0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="57da0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57da0-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57da0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="57da0-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57da0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="57da0-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57da0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="57da0-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57da0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="57da0-120">Header</span><span class="sxs-lookup"><span data-stu-id="57da0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="57da0-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="57da0-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





