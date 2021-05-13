---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste Datei-Manager auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um Menüelemente zu initialisieren.
title: FMEVENT_INITMENU Nachricht (Wfext.h)
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
ms.openlocfilehash: 82ec9130a681bdfd36ff6259392c0608e4cde9cf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842281"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="25f38-104">FMEVENT \_ INITMENU-Nachricht</span><span class="sxs-lookup"><span data-stu-id="25f38-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="25f38-105">Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste Datei-Manager auswählt.</span><span class="sxs-lookup"><span data-stu-id="25f38-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="25f38-106">Die Erweiterung kann diese Benachrichtigung verwenden, um Menüelemente zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="25f38-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="25f38-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="25f38-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f38-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25f38-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25f38-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="25f38-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25f38-110">*Hmenu*</span><span class="sxs-lookup"><span data-stu-id="25f38-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="25f38-111">Ein Handle für die Menüleiste des Datei-Managers.</span><span class="sxs-lookup"><span data-stu-id="25f38-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f38-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25f38-112">Return value</span></span>

<span data-ttu-id="25f38-113">Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="25f38-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f38-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25f38-114">Remarks</span></span>

<span data-ttu-id="25f38-115">Eine Erweiterungs-DLL empfängt diese Meldung nur, wenn der Benutzer das Menü der obersten Ebene auswählt.</span><span class="sxs-lookup"><span data-stu-id="25f38-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="25f38-116">Wenn die Erweiterung Untermenüs enthält, muss sie gleichzeitig initialisiert werden, wenn das Menü der obersten Ebene initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="25f38-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="25f38-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25f38-117">Requirements</span></span>



| <span data-ttu-id="25f38-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25f38-118">Requirement</span></span> | <span data-ttu-id="25f38-119">Wert</span><span class="sxs-lookup"><span data-stu-id="25f38-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25f38-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25f38-120">Minimum supported client</span></span><br/> | <span data-ttu-id="25f38-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25f38-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="25f38-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25f38-122">Minimum supported server</span></span><br/> | <span data-ttu-id="25f38-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25f38-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="25f38-124">Header</span><span class="sxs-lookup"><span data-stu-id="25f38-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f38-125"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="25f38-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f38-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25f38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f38-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="25f38-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




