---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Datei-Manager-Verzeichnis Fenster oder im Fenster "Suchergebnisse" auswählt.
title: FMEVENT_SELCHANGE Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: 4b05bca54f75bd48b5e710e31c31e5f0f56a2597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524504"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="76f59-103">\_Meldung zum Ändern der Nachricht</span><span class="sxs-lookup"><span data-stu-id="76f59-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="76f59-104">Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Datei-Manager-Verzeichnis Fenster oder im Fenster "Suchergebnisse" auswählt.</span><span class="sxs-lookup"><span data-stu-id="76f59-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="76f59-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="76f59-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f59-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76f59-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="76f59-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="76f59-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="76f59-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76f59-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="76f59-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="76f59-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76f59-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76f59-110">Return value</span></span>

<span data-ttu-id="76f59-111">Eine Erweiterungs-DLL sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="76f59-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f59-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76f59-112">Remarks</span></span>

<span data-ttu-id="76f59-113">Diese Meldung wird nicht durch Änderungen im Strukturbereich des Verzeichnis Fensters erzeugt.</span><span class="sxs-lookup"><span data-stu-id="76f59-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="76f59-114">Da der Benutzer die Auswahl mehrmals ändern kann, muss die Erweiterungs-DLL nach der Verarbeitung dieser Nachricht umgehend zurückgeben, um zu vermeiden, dass der Auswahl Vorgang für den Benutzer verlangsamt wird.</span><span class="sxs-lookup"><span data-stu-id="76f59-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f59-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="76f59-115">Requirements</span></span>



| <span data-ttu-id="76f59-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76f59-116">Requirement</span></span> | <span data-ttu-id="76f59-117">Wert</span><span class="sxs-lookup"><span data-stu-id="76f59-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76f59-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76f59-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76f59-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f59-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="76f59-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76f59-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76f59-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76f59-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="76f59-122">Header</span><span class="sxs-lookup"><span data-stu-id="76f59-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76f59-123"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f59-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f59-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76f59-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f59-125">**"F"**</span><span class="sxs-lookup"><span data-stu-id="76f59-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




