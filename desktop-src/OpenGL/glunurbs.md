---
title: glunurbscallback-Funktion (glu. h)
description: Die Funktion "glunurbscallback" definiert einen Rückruf für ein nicht einheitliches Rational B-Spline-Objekt (NURBS).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- glunurbscallback-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342414"
---
# <a name="glunurbscallback-function"></a><span data-ttu-id="e49c3-104">glunurbscallback-Funktion</span><span class="sxs-lookup"><span data-stu-id="e49c3-104">gluNurbsCallback function</span></span>

<span data-ttu-id="e49c3-105">Die Funktion " **glunurbscallback** " definiert einen Rückruf für ein nicht einheitliches Rational B-Spline-Objekt ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="e49c3-105">The **gluNurbsCallback** function defines a callback for a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e49c3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e49c3-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="e49c3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e49c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e49c3-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="e49c3-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="e49c3-109">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="e49c3-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="e49c3-110">*,*</span><span class="sxs-lookup"><span data-stu-id="e49c3-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="e49c3-111">Der Rückruf, der definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e49c3-111">The callback being defined.</span></span> <span data-ttu-id="e49c3-112">Der einzige gültige Wert ist "glu \_ Error".</span><span class="sxs-lookup"><span data-stu-id="e49c3-112">The only valid value is GLU\_ERROR.</span></span> <span data-ttu-id="e49c3-113">Die Bedeutung von "glu \_ Error" bedeutet, dass die Fehlerfunktion aufgerufen wird, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e49c3-113">The meaning of GLU\_ERROR means that the error function is called when an error is encountered.</span></span> <span data-ttu-id="e49c3-114">Das einzige Argument ist vom Typ " **GLenum**" und gibt den spezifischen Fehler an, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e49c3-114">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="e49c3-115">Es gibt 37-Fehler, die für nursb eindeutig sind, mit dem Namen "glu \_ nursb \_ ERROR1 through glu \_ nursb \_ ERROR37".</span><span class="sxs-lookup"><span data-stu-id="e49c3-115">There are 37 errors unique to NURBS, named GLU\_NURBS\_ERROR1 through GLU\_NURBS\_ERROR37.</span></span> <span data-ttu-id="e49c3-116">Zeichen folgen, die diese Fehler beschreiben, können mit " [**gluerrorstring**](gluerrorstring.md)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e49c3-116">Character strings describing these errors can be retrieved with [**gluErrorString**](gluerrorstring.md).</span></span>

</dd> <dt>

<span data-ttu-id="e49c3-117">*fn*</span><span class="sxs-lookup"><span data-stu-id="e49c3-117">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="e49c3-118">Ein Zeiger auf die Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="e49c3-118">A pointer to the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e49c3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e49c3-119">Return value</span></span>

<span data-ttu-id="e49c3-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e49c3-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e49c3-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e49c3-121">Remarks</span></span>

<span data-ttu-id="e49c3-122">Verwenden Sie **glunurbscallback** , um einen Rückruf zu definieren, der von einem nurb-Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e49c3-122">Use **gluNurbsCallback** to define a callback to be used by a NURBS object.</span></span> <span data-ttu-id="e49c3-123">Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e49c3-123">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="e49c3-124">Wenn *FN* **null** ist, wird ein beliebiger vorhandener Rückruf gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e49c3-124">If *fn* is **NULL**, then any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="e49c3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e49c3-125">Requirements</span></span>



| <span data-ttu-id="e49c3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e49c3-126">Requirement</span></span> | <span data-ttu-id="e49c3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e49c3-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e49c3-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e49c3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e49c3-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e49c3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e49c3-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e49c3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e49c3-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e49c3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e49c3-132">Header</span><span class="sxs-lookup"><span data-stu-id="e49c3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e49c3-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="e49c3-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e49c3-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e49c3-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="e49c3-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e49c3-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e49c3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e49c3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e49c3-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e49c3-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e49c3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e49c3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e49c3-139">**gluerrorstring**</span><span class="sxs-lookup"><span data-stu-id="e49c3-139">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="e49c3-140">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="e49c3-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





