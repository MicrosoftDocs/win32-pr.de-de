---
title: gluerrorstring-Funktion (glu. h)
description: Die Funktion "gluerrorstring" erzeugt eine Fehler Zeichenfolge aus einem OpenGL-oder glu-Fehlercode. Die Fehler Zeichenfolge ist nur ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluerrorstring-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741120"
---
# <a name="gluerrorstring-function"></a><span data-ttu-id="94346-105">gluerrorstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="94346-105">gluErrorString function</span></span>

<span data-ttu-id="94346-106">Die Funktion " **gluerrorstring** " erzeugt eine Fehler Zeichenfolge aus einem OpenGL-oder glu-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="94346-106">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="94346-107">Die Fehler Zeichenfolge ist nur ANSI.</span><span class="sxs-lookup"><span data-stu-id="94346-107">The error string is ANSI only.</span></span>

## <a name="syntax"></a><span data-ttu-id="94346-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="94346-108">Syntax</span></span>


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a><span data-ttu-id="94346-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="94346-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94346-110">*Errcode*</span><span class="sxs-lookup"><span data-stu-id="94346-110">*errCode*</span></span> 
</dt> <dd>

<span data-ttu-id="94346-111">Ein OpenGL-oder glu-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="94346-111">An OpenGL or GLU error code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94346-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94346-112">Remarks</span></span>

<span data-ttu-id="94346-113">Die Funktion " **gluerrorstring** " erzeugt eine Fehler Zeichenfolge aus einem OpenGL-oder glu-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="94346-113">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="94346-114">Die Zeichenfolge weist ein ISO Latin 1-Format auf.</span><span class="sxs-lookup"><span data-stu-id="94346-114">The string is in an ISO Latin 1 format.</span></span> <span data-ttu-id="94346-115">Beispielsweise gibt " **gluerrorstring**(GL \_ out \_ of \_ Memory)" die Zeichenfolge "nicht genügend Arbeitsspeicher" zurück.</span><span class="sxs-lookup"><span data-stu-id="94346-115">For example, **gluErrorString**(GL\_OUT\_OF\_MEMORY) returns the string "out of memory".</span></span>

<span data-ttu-id="94346-116">Die standardmäßigen glu-Fehlercodes lauten "glu \_ invalid \_ enum", "glu \_ invalid value" und "glu" aus dem Arbeits \_ \_ \_ \_ Speicher.</span><span class="sxs-lookup"><span data-stu-id="94346-116">The standard GLU error codes are GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY.</span></span> <span data-ttu-id="94346-117">Bestimmte andere glu-Funktionen können spezielle Fehlercodes durch Rückrufe zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="94346-117">Certain other GLU functions can return specialized error codes through callbacks.</span></span> <span data-ttu-id="94346-118">Eine Liste der OpenGL-Fehlercodes finden Sie unter [**glgeterror**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="94346-118">For the list of OpenGL error codes, see [**glGetError**](glgeterror.md).</span></span>

<span data-ttu-id="94346-119">Die Funktion " **gluerrorstring** " erzeugt Fehler Zeichenfolgen nur in ANSI.</span><span class="sxs-lookup"><span data-stu-id="94346-119">The **gluErrorString** function produces error strings in ANSI only.</span></span> <span data-ttu-id="94346-120">Verwenden Sie nach Möglichkeit " **gluerrorstringwin**", das ANSI-oder Unicode-Fehler Zeichenfolgen zulässt.</span><span class="sxs-lookup"><span data-stu-id="94346-120">Whenever possible, use **gluErrorStringWIN**, which allows ANSI or Unicode error strings.</span></span> <span data-ttu-id="94346-121">Dadurch ist es einfacher, Ihr Programm für die Verwendung mit einer anderen Sprache zu lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="94346-121">This makes it easier to localize your program for use with another language.</span></span>

## <a name="requirements"></a><span data-ttu-id="94346-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94346-122">Requirements</span></span>



| <span data-ttu-id="94346-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94346-123">Requirement</span></span> | <span data-ttu-id="94346-124">Wert</span><span class="sxs-lookup"><span data-stu-id="94346-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="94346-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94346-125">Minimum supported client</span></span><br/> | <span data-ttu-id="94346-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94346-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="94346-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94346-127">Minimum supported server</span></span><br/> | <span data-ttu-id="94346-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94346-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="94346-129">Header</span><span class="sxs-lookup"><span data-stu-id="94346-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="94346-130"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="94346-130"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="94346-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94346-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="94346-132"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94346-132"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94346-133">DLL</span><span class="sxs-lookup"><span data-stu-id="94346-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94346-134"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94346-134"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94346-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94346-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94346-136">**glgeterror**</span><span class="sxs-lookup"><span data-stu-id="94346-136">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="94346-137">*glunurbscallback*</span><span class="sxs-lookup"><span data-stu-id="94346-137">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="94346-138">*gluvierccallback*</span><span class="sxs-lookup"><span data-stu-id="94346-138">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="94346-139">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="94346-139">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





