---
description: Gibt einen Zeiger auf den Kommentar einer Aufzeichnung zurück.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Getcapturecomment-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346685"
---
# <a name="getcapturecomment-function"></a><span data-ttu-id="f8cc0-103">Getcapturecomment-Funktion</span><span class="sxs-lookup"><span data-stu-id="f8cc0-103">GetCaptureComment function</span></span>

<span data-ttu-id="f8cc0-104">Die **getcapturecomment** -Funktion gibt einen Zeiger auf den Kommentar einer Aufzeichnung zurück.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-104">The **GetCaptureComment** function returns a pointer to the comment of a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8cc0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8cc0-105">Syntax</span></span>


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="f8cc0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8cc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8cc0-107">*hcapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8cc0-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8cc0-108">Ein Handle für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-108">A handle to the capture.</span></span> <span data-ttu-id="f8cc0-109">Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="f8cc0-109">For more information about obtaining the capture handle, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8cc0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8cc0-110">Return value</span></span>

<span data-ttu-id="f8cc0-111">Wenn die Funktion erfolgreich ist (d. h., wenn die Erfassung einen Kommentar enthält), ist der Rückgabewert ein Zeiger auf die Kommentar Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-111">If the function is successful (that is, if the capture contains a comment), the return value is a pointer to the comment string.</span></span>

<span data-ttu-id="f8cc0-112">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8cc0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8cc0-113">Remarks</span></span>

<span data-ttu-id="f8cc0-114">Ändern Sie die zurückgegebene Kommentar Zeichenfolge nicht, da es sich um die tatsächliche Kommentar Zeichenfolge in der geladenen Erfassung handelt.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-114">Do not alter the returned comment string which is the actual comment string that is in the loaded capture.</span></span> <span data-ttu-id="f8cc0-115">Alle Änderungen können die Erfassung beschädigen.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-115">Any changes can corrupt the capture.</span></span> <span data-ttu-id="f8cc0-116">Versuche, die Zeichenfolge zu ändern, führen zu einer Zugriffsverletzung.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-116">Attempts to modify the string result in an access violation.</span></span>

<span data-ttu-id="f8cc0-117">Das Handle der Erfassung kann auf verschiedene Weise abgerufen werden, je nachdem, ob der-Befehl von einem Experten oder Parser aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-117">The handle of the capture can be obtained in several ways, depending if the call is made by an expert or parser.</span></span> <span data-ttu-id="f8cc0-118">Für Experten wird das Handle im **hcapture** -Member der " [expertstartupinfo](expertstartupinfo.md) "-Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-118">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="f8cc0-119">Für Parser kann das Erfassungs Handle abgerufen werden, indem die [getframecapturehandle](getframecapturehandle.md) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-119">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="f8cc0-120">Um den Kommentar einer Erfassung aus der Erfassungs Datei abzurufen, rufen Sie die [getcapturecommentfromfilename](getcapturecommentfromfilename.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-120">To retrieve the comment of a capture from its capture file, call the [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) function.</span></span>

<span data-ttu-id="f8cc0-121">[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturecomment** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f8cc0-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureComment** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8cc0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8cc0-122">Requirements</span></span>



| <span data-ttu-id="f8cc0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8cc0-123">Requirement</span></span> | <span data-ttu-id="f8cc0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f8cc0-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cc0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8cc0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f8cc0-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8cc0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f8cc0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8cc0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f8cc0-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8cc0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f8cc0-129">Header</span><span class="sxs-lookup"><span data-stu-id="f8cc0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8cc0-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8cc0-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f8cc0-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8cc0-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8cc0-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8cc0-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8cc0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f8cc0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8cc0-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8cc0-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8cc0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8cc0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8cc0-136">Expertstartupinfo</span><span class="sxs-lookup"><span data-stu-id="f8cc0-136">EXPERTSTARTUPINFO</span></span>](expertstartupinfo.md)
</dt> <dt>

[<span data-ttu-id="f8cc0-137">Getcapturecommentfromfilename</span><span class="sxs-lookup"><span data-stu-id="f8cc0-137">GetCaptureCommentFromFilename</span></span>](getcapturecommentfromfilename.md)
</dt> <dt>

[<span data-ttu-id="f8cc0-138">Getframecapturehandle</span><span class="sxs-lookup"><span data-stu-id="f8cc0-138">GetFrameCaptureHandle</span></span>](getframecapturehandle.md)
</dt> </dl>

 

 




