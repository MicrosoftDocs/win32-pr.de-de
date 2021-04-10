---
title: MCIWNDM_NOTIFYMODE Meldung (VFW. h)
description: Die mciwndm \_ notifymode-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich der Betriebsmodus des MCI-Geräts geändert hat.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040074"
---
# <a name="mciwndm_notifymode-message"></a><span data-ttu-id="7182e-104">Mciwndm \_ notifymode-Meldung</span><span class="sxs-lookup"><span data-stu-id="7182e-104">MCIWNDM\_NOTIFYMODE message</span></span>

<span data-ttu-id="7182e-105">Die **mciwndm \_ notifymode** -Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich der Betriebsmodus des MCI-Geräts geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7182e-105">The **MCIWNDM\_NOTIFYMODE** message notifies the parent window of an application that the operating mode of the MCI device has changed.</span></span>


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a><span data-ttu-id="7182e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7182e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7182e-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="7182e-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="7182e-108">Handle für das mciwnd-Fenster.</span><span class="sxs-lookup"><span data-stu-id="7182e-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="7182e-109"><span id="mode"></span><span id="MODE"></span>*Spar*</span><span class="sxs-lookup"><span data-stu-id="7182e-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="7182e-110">Eine Ganzzahl, die dem MCI-Modus entspricht.</span><span class="sxs-lookup"><span data-stu-id="7182e-110">Integer corresponding to the MCI mode.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7182e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7182e-111">Remarks</span></span>

<span data-ttu-id="7182e-112">Sie können Benachrichtigungen über Änderungen im Modus eines MCI-Geräts aktivieren, indem Sie den mciwndf- \_ Fenster Stil "notifymode" angeben.</span><span class="sxs-lookup"><span data-stu-id="7182e-112">You can enable notification of mode changes of an MCI device by specifying the MCIWNDF\_NOTIFYMODE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="7182e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7182e-113">Requirements</span></span>



| <span data-ttu-id="7182e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7182e-114">Requirement</span></span> | <span data-ttu-id="7182e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7182e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7182e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7182e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7182e-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7182e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7182e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7182e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7182e-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7182e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7182e-120">Header</span><span class="sxs-lookup"><span data-stu-id="7182e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7182e-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7182e-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





