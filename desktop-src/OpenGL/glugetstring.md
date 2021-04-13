---
title: glugetstring-Funktion (glu. h)
description: Die Funktion "glugetstring" Ruft eine Zeichenfolge ab, die die glu-Versionsnummer oder unterstützte glu-Erweiterungs Aufrufe beschreibt.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- glugetstring-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391813"
---
# <a name="glugetstring-function"></a><span data-ttu-id="04d97-104">glugetstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="04d97-104">gluGetString function</span></span>

<span data-ttu-id="04d97-105">Die Funktion " **glugetstring** " Ruft eine Zeichenfolge ab, die die glu-Versionsnummer oder unterstützte glu-Erweiterungs Aufrufe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="04d97-105">The **gluGetString** function gets a string that describes the GLU version number or supported GLU extension calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d97-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="04d97-106">Syntax</span></span>


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="04d97-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="04d97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d97-108">*name*</span><span class="sxs-lookup"><span data-stu-id="04d97-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="04d97-109">Entweder die Versionsnummer von Glu (GLU \_ Version) oder die verfügbaren herstellerspezifischen Erweiterungs Aufrufe (GLU \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="04d97-109">Either the version number of GLU (GLU\_VERSION) or available vendor-specific extension calls (GLU\_EXTENSIONS).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04d97-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04d97-110">Remarks</span></span>

<span data-ttu-id="04d97-111">Die Funktion " **glugetstring** " gibt einen Zeiger auf eine statische, auf NULL endenden Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="04d97-111">The **gluGetString** function returns a pointer to a static, null-terminated string.</span></span> <span data-ttu-id="04d97-112">Wenn *Name* den Wert "- \_ Version" hat, ist die zurückgegebene Zeichenfolge ein Wert, der die Versionsnummer von Glu darstellt.</span><span class="sxs-lookup"><span data-stu-id="04d97-112">When *name* is GLU\_VERSION, the returned string is a value that represents the version number of GLU.</span></span> <span data-ttu-id="04d97-113">Das Format der Versionsnummer lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="04d97-113">The format of the version number is as follows:</span></span>

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

<span data-ttu-id="04d97-114">Die Versionsnummer hat das Format "Haupt \_ Nummer. neben \_ Nummer" oder "Haupt \_ Nummer. neben \_ Version. \_ Releasenummer".</span><span class="sxs-lookup"><span data-stu-id="04d97-114">The version number has the form "major\_number.minor\_number" or "major\_number.minor\_number.release\_number".</span></span> <span data-ttu-id="04d97-115">Die anbieterspezifischen Informationen sind optional, und das Format und der Inhalt hängen von der Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="04d97-115">The vendor-specific information is optional, and the format and contents depend on the implementation.</span></span>

<span data-ttu-id="04d97-116">Wenn *Name* der Wert "-Erweiterungen" ist \_ , enthält die zurückgegebene Zeichenfolge eine Liste mit Namen unterstützter glu-Erweiterungen, die durch Leerzeichen getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="04d97-116">When *name* is GLU\_EXTENSIONS, the returned string contains a list of names of supported GLU extensions that are separated by spaces.</span></span> <span data-ttu-id="04d97-117">Das Format der zurückgegebenen Liste von Namen lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="04d97-117">The format of the returned list of names is as follows:</span></span>

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

<span data-ttu-id="04d97-118">Die Erweiterungs Namen dürfen keine Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="04d97-118">The extension names cannot contain any spaces.</span></span>

<span data-ttu-id="04d97-119">Die Funktion " **glugetstring** " ist gültig für die Version 1,1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="04d97-119">The **gluGetString** function is valid for GLU version 1.1 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d97-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04d97-120">Requirements</span></span>



| <span data-ttu-id="04d97-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04d97-121">Requirement</span></span> | <span data-ttu-id="04d97-122">Wert</span><span class="sxs-lookup"><span data-stu-id="04d97-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04d97-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04d97-123">Minimum supported client</span></span><br/> | <span data-ttu-id="04d97-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04d97-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="04d97-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04d97-125">Minimum supported server</span></span><br/> | <span data-ttu-id="04d97-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04d97-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="04d97-127">Header</span><span class="sxs-lookup"><span data-stu-id="04d97-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="04d97-128"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="04d97-128"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="04d97-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04d97-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="04d97-130"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04d97-130"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="04d97-131">DLL</span><span class="sxs-lookup"><span data-stu-id="04d97-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04d97-132"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d97-132"><dt>Glu32.dll</dt></span></span> </dl> |



 

 





