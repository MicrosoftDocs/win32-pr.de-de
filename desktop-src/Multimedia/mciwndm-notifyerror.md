---
title: MCIWNDM_NOTIFYERROR Meldung (VFW. h)
description: Die mciwndm \_ notifyerror-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass ein MCI-Fehler aufgetreten ist.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040479"
---
# <a name="mciwndm_notifyerror-message"></a><span data-ttu-id="e3a80-104">Mciwndm \_ notifyerror-Meldung</span><span class="sxs-lookup"><span data-stu-id="e3a80-104">MCIWNDM\_NOTIFYERROR message</span></span>

<span data-ttu-id="e3a80-105">Die **mciwndm \_ notifyerror** -Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass ein MCI-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e3a80-105">The **MCIWNDM\_NOTIFYERROR** message notifies the parent window of an application that an MCI error occurred.</span></span>


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a><span data-ttu-id="e3a80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3a80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a80-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="e3a80-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="e3a80-108">Handle für das mciwnd-Fenster.</span><span class="sxs-lookup"><span data-stu-id="e3a80-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="e3a80-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*ErrorCode*</span><span class="sxs-lookup"><span data-stu-id="e3a80-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span></span>
</dt> <dd>

<span data-ttu-id="e3a80-110">Numerischer Code für den MCI-Fehler.</span><span class="sxs-lookup"><span data-stu-id="e3a80-110">Numerical code for the MCI error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3a80-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3a80-111">Remarks</span></span>

<span data-ttu-id="e3a80-112">Sie können die MCI-Fehler Benachrichtigung aktivieren, indem Sie den Fenster Stil "mciwndf \_ notifyerror" angeben.</span><span class="sxs-lookup"><span data-stu-id="e3a80-112">You can enable MCI error notification by specifying the MCIWNDF\_NOTIFYERROR window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a80-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3a80-113">Requirements</span></span>



| <span data-ttu-id="e3a80-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3a80-114">Requirement</span></span> | <span data-ttu-id="e3a80-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e3a80-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e3a80-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3a80-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a80-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3a80-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e3a80-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3a80-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a80-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3a80-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e3a80-120">Header</span><span class="sxs-lookup"><span data-stu-id="e3a80-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a80-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a80-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





