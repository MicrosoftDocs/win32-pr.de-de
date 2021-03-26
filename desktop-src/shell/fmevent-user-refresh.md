---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer im Datei-Manager im Menü Ansicht den Befehl Aktualisieren auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um das Menü zu aktualisieren.
title: FMEVENT_USER_REFRESH Meldung (WF. h)
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
ms.openlocfilehash: c3c4596b0ea589545c6e59953b9c7b5977e07b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979704"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="eb863-104">\_Meldung zum Aktualisieren von Benutzer \_ Meldungen</span><span class="sxs-lookup"><span data-stu-id="eb863-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="eb863-105">Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer im Datei-Manager im Menü **Ansicht** den Befehl **Aktualisieren** auswählt.</span><span class="sxs-lookup"><span data-stu-id="eb863-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="eb863-106">Die Erweiterung kann diese Benachrichtigung verwenden, um das Menü zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="eb863-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb863-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb863-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb863-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb863-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eb863-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="eb863-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eb863-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb863-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eb863-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="eb863-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb863-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb863-112">Return value</span></span>

<span data-ttu-id="eb863-113">Eine Erweiterungs-DLL sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="eb863-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb863-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="eb863-114">Requirements</span></span>



| <span data-ttu-id="eb863-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb863-115">Requirement</span></span> | <span data-ttu-id="eb863-116">Wert</span><span class="sxs-lookup"><span data-stu-id="eb863-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb863-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb863-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eb863-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb863-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="eb863-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb863-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eb863-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb863-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eb863-121">Header</span><span class="sxs-lookup"><span data-stu-id="eb863-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb863-122"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb863-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb863-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb863-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb863-124">**"F"**</span><span class="sxs-lookup"><span data-stu-id="eb863-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




