---
description: Die getcapturecommentfromfilename-Funktion extrahiert den Erfassungs Kommentar aus einer Erfassungs Datei.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Getcapturecommentfromfilename-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345002"
---
# <a name="getcapturecommentfromfilename-function"></a><span data-ttu-id="aa793-103">Getcapturecommentfromfilename-Funktion</span><span class="sxs-lookup"><span data-stu-id="aa793-103">GetCaptureCommentFromFilename function</span></span>

<span data-ttu-id="aa793-104">Die **getcapturecommentfromfilename** -Funktion extrahiert den Erfassungs Kommentar aus einer [*Erfassungs Datei*](c.md).</span><span class="sxs-lookup"><span data-stu-id="aa793-104">The **GetCaptureCommentFromFilename** function extracts the capture comment from a [*capture file*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa793-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa793-105">Syntax</span></span>


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="aa793-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa793-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa793-107">*lpFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa793-107">*lpFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa793-108">Zeiger auf den Namen der Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="aa793-108">Pointer to the name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="aa793-109">*lpcomment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa793-109">*lpComment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa793-110">Zeiger auf eine vorab zugeordnete Zeichenfolge für den Kommentar.</span><span class="sxs-lookup"><span data-stu-id="aa793-110">Pointer to a pre-allocated string for the comment.</span></span>

</dd> <dt>

<span data-ttu-id="aa793-111">*BufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa793-111">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa793-112">Größe der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="aa793-112">Size of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa793-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa793-113">Return value</span></span>

<span data-ttu-id="aa793-114">Wenn die Funktion erfolgreich ist (d. h., wenn der Kommentar gefunden und kopiert wird oder kein Kommentar in der Erfassungs Datei vorhanden ist), ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="aa793-114">If the function is successful (that is, if the comment is found and copied, or there is no comment in the capture file), the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="aa793-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="aa793-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="aa793-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="aa793-116">Return code</span></span>                                                                                                 | <span data-ttu-id="aa793-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa793-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa793-118"><dt>**nmerr- \_ Datei \_ Lese \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="aa793-118"><dt>**NMERR\_FILE\_READ\_ERROR**</dt></span></span> </dl>     | <span data-ttu-id="aa793-119">Der Erfassungs Kommentar kann nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="aa793-119">The capture comment cannot be read.</span></span><br/>                               |
| <dl> <span data-ttu-id="aa793-120"><dt>**Ungültiges nmerr- \_ \_ Datei \_ Format**</dt></span><span class="sxs-lookup"><span data-stu-id="aa793-120"><dt>**NMERR\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="aa793-121">Der Kommentar Rahmen ist kein gültiges Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="aa793-121">The Comment frame is not a valid file format.</span></span><br/>                     |
| <dl> <span data-ttu-id="aa793-122"><dt>**die nmerr- \_ Datei wurde \_ nicht \_ gefunden.**</dt></span><span class="sxs-lookup"><span data-stu-id="aa793-122"><dt>**NMERR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>      | <span data-ttu-id="aa793-123">Die vom *lpFileName* -Parameter angegebene Datei kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="aa793-123">The file specified by the *lpFilename* parameter cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="aa793-124"><dt>**Ungültiger nmerr- \_ \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="aa793-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="aa793-125">Einer der Parameter ist falsch angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa793-125">One of the parameters is specified incorrectly.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="aa793-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa793-126">Remarks</span></span>

<span data-ttu-id="aa793-127">[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturecommentfromfilename** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aa793-127">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureCommentFromFilename** function.</span></span>

<span data-ttu-id="aa793-128">Um den Kommentar einer echt Zeiterfassung abzurufen, rufen Sie die [getcapturecomment](getcapturecomment.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="aa793-128">To retrieve the comment of a real-time capture, call the [GetCaptureComment](getcapturecomment.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa793-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa793-129">Requirements</span></span>



| <span data-ttu-id="aa793-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa793-130">Requirement</span></span> | <span data-ttu-id="aa793-131">Wert</span><span class="sxs-lookup"><span data-stu-id="aa793-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa793-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa793-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aa793-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa793-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aa793-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa793-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aa793-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa793-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aa793-136">Header</span><span class="sxs-lookup"><span data-stu-id="aa793-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa793-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa793-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="aa793-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa793-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa793-139"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa793-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="aa793-140">DLL</span><span class="sxs-lookup"><span data-stu-id="aa793-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa793-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa793-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa793-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa793-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa793-143">Getcapturecomment</span><span class="sxs-lookup"><span data-stu-id="aa793-143">GetCaptureComment</span></span>](getcapturecomment.md)
</dt> </dl>

 

 




