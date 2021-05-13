---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Datei-Manager-Verzeichnisfenster oder im Fenster Suchergebnisse auswählt.
title: FMEVENT_SELCHANGE Nachricht (Wfext.h)
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
ms.openlocfilehash: e9aa647434aab5a483626757179a7b23b3372a02
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842261"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="f14c7-103">FMEVENT \_ SELCHANGE-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f14c7-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="f14c7-104">Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer einen Dateinamen im Datei-Manager-Verzeichnisfenster oder im Fenster Suchergebnisse auswählt.</span><span class="sxs-lookup"><span data-stu-id="f14c7-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="f14c7-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f14c7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f14c7-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f14c7-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f14c7-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f14c7-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f14c7-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f14c7-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f14c7-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f14c7-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f14c7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f14c7-110">Return value</span></span>

<span data-ttu-id="f14c7-111">Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f14c7-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f14c7-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f14c7-112">Remarks</span></span>

<span data-ttu-id="f14c7-113">Änderungen am Strukturteil des Verzeichnisfensters erzeugen diese Meldung nicht.</span><span class="sxs-lookup"><span data-stu-id="f14c7-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="f14c7-114">Da der Benutzer die Auswahl mehrmals ändern kann, muss die Erweiterungs-DLL nach der Verarbeitung dieser Meldung sofort zurückgeben, um eine Verlangsamung des Auswahlprozesses für den Benutzer zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f14c7-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="f14c7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f14c7-115">Requirements</span></span>



| <span data-ttu-id="f14c7-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f14c7-116">Requirement</span></span> | <span data-ttu-id="f14c7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f14c7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f14c7-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f14c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f14c7-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f14c7-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f14c7-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f14c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f14c7-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f14c7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f14c7-122">Header</span><span class="sxs-lookup"><span data-stu-id="f14c7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f14c7-123"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="f14c7-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f14c7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f14c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14c7-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="f14c7-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




