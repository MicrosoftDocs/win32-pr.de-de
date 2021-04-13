---
title: EM_INSERTIMAGE Meldung (RichEdit. h)
description: Ersetzt die Auswahl durch ein BLOB, das ein Bild anzeigt.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- Windows-Steuerelemente für EM_INSERTIMAGE Meldung
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475558"
---
# <a name="em_insertimage-message"></a><span data-ttu-id="5d316-104">EM \_ InsertImage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5d316-104">EM\_INSERTIMAGE message</span></span>

<span data-ttu-id="5d316-105">Ersetzt die Auswahl durch ein BLOB, das ein Bild anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5d316-105">Replaces the selection with a blob that displays an image.</span></span>


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a><span data-ttu-id="5d316-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d316-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d316-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d316-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5d316-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5d316-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d316-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d316-110">Ein Zeiger auf eine [**RichEdit- \_ Bild \_ Parameter**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) Struktur, die das bildblob enthält.</span><span class="sxs-lookup"><span data-stu-id="5d316-110">A pointer to a [**RICHEDIT\_IMAGE\_PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) structure that contains the image blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d316-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d316-111">Return value</span></span>

<span data-ttu-id="5d316-112">Gibt \_ bei Erfolg S OK oder einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="5d316-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="5d316-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5d316-113">Return code</span></span>                                                                                    | <span data-ttu-id="5d316-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d316-114">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="5d316-115"><dt>**E \_** Fehler</dt></span><span class="sxs-lookup"><span data-stu-id="5d316-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="5d316-116">Das Bild kann nicht eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5d316-116">Cannot insert the image.</span></span> <br/>                          |
| <dl> <span data-ttu-id="5d316-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="5d316-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="5d316-118">Der *LPARAM* -Parameter ist NULL oder zeigt auf ein ungültiges Bild.</span><span class="sxs-lookup"><span data-stu-id="5d316-118">The *lParam* parameter is NULL or points to an invalid image.</span></span> |
| <dl> <span data-ttu-id="5d316-119"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="5d316-119"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="5d316-120">Es ist nicht genügend Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d316-120">Insufficient memory is available.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5d316-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d316-121">Remarks</span></span>

<span data-ttu-id="5d316-122">Wenn es sich bei der Auswahl um eine Einfügemarke handelt, wird das imageblob an der Einfügemarke eingefügt.</span><span class="sxs-lookup"><span data-stu-id="5d316-122">If the selection is an insertion point, the image blob is inserted at the insertion point.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d316-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d316-123">Requirements</span></span>



| <span data-ttu-id="5d316-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d316-124">Requirement</span></span> | <span data-ttu-id="5d316-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5d316-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d316-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d316-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5d316-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d316-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5d316-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d316-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5d316-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d316-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d316-130">Header</span><span class="sxs-lookup"><span data-stu-id="5d316-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d316-131"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d316-131"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d316-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d316-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d316-133">**EM \_ inserables**</span><span class="sxs-lookup"><span data-stu-id="5d316-133">**EM\_INSERTTABLE**</span></span>](em-inserttable.md)
</dt> </dl>

 

 





