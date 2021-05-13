---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer im Menü Ansicht im Datei-Manager den Befehl Aktualisieren ausgibt. Die Erweiterung kann diese Benachrichtigung verwenden, um ihr Menü zu aktualisieren.
title: FMEVENT_USER_REFRESH Nachricht (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: 16f75f562149b50237a6b41bf2023d1f694741e3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841261"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="de252-104">FMEVENT \_ USER \_ REFRESH-Nachricht</span><span class="sxs-lookup"><span data-stu-id="de252-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="de252-105">Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer im Menü **Ansicht** im Datei-Manager den Befehl **Aktualisieren** ausgibt.</span><span class="sxs-lookup"><span data-stu-id="de252-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="de252-106">Die Erweiterung kann diese Benachrichtigung verwenden, um ihr Menü zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="de252-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="de252-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="de252-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de252-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de252-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="de252-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="de252-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="de252-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de252-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="de252-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="de252-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de252-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de252-112">Return value</span></span>

<span data-ttu-id="de252-113">Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="de252-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="de252-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de252-114">Requirements</span></span>



| <span data-ttu-id="de252-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de252-115">Requirement</span></span> | <span data-ttu-id="de252-116">Wert</span><span class="sxs-lookup"><span data-stu-id="de252-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de252-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de252-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de252-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de252-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="de252-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de252-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de252-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de252-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="de252-121">Header</span><span class="sxs-lookup"><span data-stu-id="de252-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de252-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="de252-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de252-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de252-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de252-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="de252-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




