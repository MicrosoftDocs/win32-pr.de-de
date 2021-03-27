---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste des Datei-Managers auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um Menü Elemente zu initialisieren.
title: FMEVENT_INITMENU Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 4bbb959feeb2c1bf99eaa999b4c51b69b0d0cf63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214304"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="d4ac0-104">Meldung zu "smevent \_ InitMenu"</span><span class="sxs-lookup"><span data-stu-id="d4ac0-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="d4ac0-105">Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste des Datei-Managers auswählt.</span><span class="sxs-lookup"><span data-stu-id="d4ac0-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="d4ac0-106">Die Erweiterung kann diese Benachrichtigung verwenden, um Menü Elemente zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d4ac0-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4ac0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4ac0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ac0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4ac0-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d4ac0-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d4ac0-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d4ac0-110">*HMENU*</span><span class="sxs-lookup"><span data-stu-id="d4ac0-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ac0-111">Ein Handle für die Menüleiste des Datei-Managers.</span><span class="sxs-lookup"><span data-stu-id="d4ac0-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ac0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4ac0-112">Return value</span></span>

<span data-ttu-id="d4ac0-113">Eine Erweiterungs-DLL sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d4ac0-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4ac0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4ac0-114">Remarks</span></span>

<span data-ttu-id="d4ac0-115">Eine Erweiterungs-DLL empfängt diese Nachricht nur, wenn der Benutzer das Menü der obersten Ebene auswählt.</span><span class="sxs-lookup"><span data-stu-id="d4ac0-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="d4ac0-116">Wenn die Erweiterung Untermenüs enthält, muss Sie gleichzeitig initialisiert werden, wenn Sie das Menü der obersten Ebene initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d4ac0-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ac0-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d4ac0-117">Requirements</span></span>



| <span data-ttu-id="d4ac0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4ac0-118">Requirement</span></span> | <span data-ttu-id="d4ac0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d4ac0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ac0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4ac0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ac0-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4ac0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d4ac0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4ac0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ac0-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4ac0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d4ac0-124">Header</span><span class="sxs-lookup"><span data-stu-id="d4ac0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ac0-125"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ac0-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ac0-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4ac0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ac0-127">**"F"**</span><span class="sxs-lookup"><span data-stu-id="d4ac0-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




