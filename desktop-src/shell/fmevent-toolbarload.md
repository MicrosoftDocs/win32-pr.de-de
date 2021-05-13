---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager seine Symbolleiste lädt. Diese Meldung ermöglicht einer Erweiterungs-DLL, der Symbolleiste des Datei-Managers eine Schaltfläche hinzuzufügen.
title: FMEVENT_TOOLBARLOAD Nachricht (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: c4195acedbd696679a2deea2f4d6e268717566d1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841271"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="ed67e-104">FMEVENT \_ TOOLBARLOAD-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ed67e-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="ed67e-105">Wird an eine Erweiterungs-DLL gesendet, wenn der Datei-Manager seine Symbolleiste lädt.</span><span class="sxs-lookup"><span data-stu-id="ed67e-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="ed67e-106">Diese Meldung ermöglicht einer Erweiterungs-DLL, der Symbolleiste des Datei-Managers eine Schaltfläche hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed67e-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed67e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed67e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed67e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed67e-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ed67e-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ed67e-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ed67e-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="ed67e-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="ed67e-111">Die Adresse einer [**FMS \_ TOOLBARLOAD-Struktur.**](fms-toolbarload.md)</span><span class="sxs-lookup"><span data-stu-id="ed67e-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="ed67e-112">Wenn die Erweiterungs-DLL der Symbolleiste im Datei-Manager eine Schaltfläche hinzufügt, sollte die DLL die Struktur mit Informationen zur Schaltfläche füllen.</span><span class="sxs-lookup"><span data-stu-id="ed67e-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed67e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed67e-113">Return value</span></span>

<span data-ttu-id="ed67e-114">Eine Erweiterungs-DLL muss **TRUE** zurückgeben, um die Schaltfläche zur Symbolleiste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed67e-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="ed67e-115">Wenn die DLL **FALSE** zurückgibt, fügt der Datei-Manager die Schaltfläche nicht hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed67e-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed67e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed67e-116">Requirements</span></span>



| <span data-ttu-id="ed67e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed67e-117">Requirement</span></span> | <span data-ttu-id="ed67e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ed67e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed67e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed67e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ed67e-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed67e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ed67e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed67e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ed67e-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed67e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ed67e-123">Header</span><span class="sxs-lookup"><span data-stu-id="ed67e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed67e-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="ed67e-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed67e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed67e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed67e-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="ed67e-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




