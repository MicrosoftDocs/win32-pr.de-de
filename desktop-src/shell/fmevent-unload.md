---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL entladen wird.
title: FMEVENT_UNLOAD Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 140fbdc79980a2ab6ba9f50b8815429436df0d3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127864"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="534a0-103">Meldung zum Entladen des Ereignisses \_</span><span class="sxs-lookup"><span data-stu-id="534a0-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="534a0-104">Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager die DLL entladen wird.</span><span class="sxs-lookup"><span data-stu-id="534a0-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="534a0-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="534a0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="534a0-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="534a0-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="534a0-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="534a0-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="534a0-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="534a0-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="534a0-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="534a0-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="534a0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="534a0-110">Return value</span></span>

<span data-ttu-id="534a0-111">Eine Erweiterungs-DLL sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="534a0-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="534a0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="534a0-112">Remarks</span></span>

<span data-ttu-id="534a0-113">Die *HWND* -und **HMENU** -Werte, die mit den " [**fmevent \_ Load**](fmevent-load.md) "-und " [**fmevent \_ InitMenu**](fmevent-initmenu.md) "-Meldungen übergeben werden, sind möglicherweise zum Zeitpunkt der Übermittlung dieser Nachricht ungültig.</span><span class="sxs-lookup"><span data-stu-id="534a0-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="534a0-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="534a0-114">Requirements</span></span>



| <span data-ttu-id="534a0-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="534a0-115">Requirement</span></span> | <span data-ttu-id="534a0-116">Wert</span><span class="sxs-lookup"><span data-stu-id="534a0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="534a0-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="534a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="534a0-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="534a0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="534a0-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="534a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="534a0-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="534a0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="534a0-121">Header</span><span class="sxs-lookup"><span data-stu-id="534a0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="534a0-122"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="534a0-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="534a0-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="534a0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534a0-124">**"F"**</span><span class="sxs-lookup"><span data-stu-id="534a0-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




