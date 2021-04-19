---
title: glgetpointerv-Funktion (GL. h)
description: Die Funktion "glgetpointerv" gibt die Adresse eines Vertex-Daten Arrays zurück.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glgetpointerv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338757"
---
# <a name="glgetpointerv-function"></a><span data-ttu-id="235ab-104">glgetpointerv-Funktion</span><span class="sxs-lookup"><span data-stu-id="235ab-104">glGetPointerv function</span></span>

<span data-ttu-id="235ab-105">Die Funktion " **glgetpointerv** " gibt die Adresse eines Vertex-Daten Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="235ab-105">The **glGetPointerv** function returns the address of a vertex data array.</span></span>

## <a name="syntax"></a><span data-ttu-id="235ab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="235ab-106">Syntax</span></span>


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a><span data-ttu-id="235ab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="235ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235ab-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="235ab-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="235ab-109">Der Typ des Array Zeigers, der von den folgenden symbolischen Konstanten zurückgegeben werden soll: GL- \_ Farb \_ array \_ Zeiger, GL- \_ \_ \_ \_ \_ \_ edgeflag-Array Zeiger, GL-Feedback \_ -Puffer Zeiger, GL \_ \_ -Index Array \_ Zeiger, GL- \_ normaler \_ array \_ Zeiger, GL \_ -Textur- \_ \_ array \_ Zeiger, GL \_ \_ -Auswahl Puffer \_ Zeiger und GL/ \_ tex- \_ array \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="235ab-109">The type of array pointer to return from the following symbolic constants: GL\_COLOR\_ARRAY\_POINTER, GL\_EDGE\_FLAG\_ARRAY\_POINTER, GL\_FEEDBACK\_BUFFER\_POINTER, GL\_INDEX\_ARRAY\_POINTER, GL\_NORMAL\_ARRAY\_POINTER, GL\_TEXTURE\_COORD\_ARRAY\_POINTER, GL\_SELECTION\_BUFFER\_POINTER, and GL\_VERTEX\_ARRAY\_POINTER.</span></span>

</dd> <dt>

<span data-ttu-id="235ab-110">*params*</span><span class="sxs-lookup"><span data-stu-id="235ab-110">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="235ab-111">Gibt den Wert des durch " *PName*" angegebenen Array Zeigers zurück.</span><span class="sxs-lookup"><span data-stu-id="235ab-111">Returns the value of the array pointer specified by *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235ab-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="235ab-112">Return value</span></span>

<span data-ttu-id="235ab-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="235ab-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="235ab-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="235ab-114">Error codes</span></span>

<span data-ttu-id="235ab-115">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="235ab-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="235ab-116">Name</span><span class="sxs-lookup"><span data-stu-id="235ab-116">Name</span></span>                                                                                             | <span data-ttu-id="235ab-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="235ab-117">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="235ab-118"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="235ab-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="235ab-119">*PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="235ab-119">*pname* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="235ab-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="235ab-120">Remarks</span></span>

<span data-ttu-id="235ab-121">Die Funktion " **glgetpointerv** " gibt Array Zeiger Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="235ab-121">The **glGetPointerv** function returns array pointer information.</span></span> <span data-ttu-id="235ab-122">Der *PName* -Parameter ist eine symbolische Konstante, die die Art des zurück zugebende Array Zeigers angibt, und *params* ist ein Zeiger auf einen Speicherort, um die zurückgegebenen Daten zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="235ab-122">The *pname* parameter is a symbolic constant specifying the kind of array pointer to return, and *params* is a pointer to a location to place the returned data.</span></span>

## <a name="requirements"></a><span data-ttu-id="235ab-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="235ab-123">Requirements</span></span>



| <span data-ttu-id="235ab-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="235ab-124">Requirement</span></span> | <span data-ttu-id="235ab-125">Wert</span><span class="sxs-lookup"><span data-stu-id="235ab-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="235ab-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="235ab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="235ab-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="235ab-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="235ab-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="235ab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="235ab-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="235ab-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="235ab-130">Header</span><span class="sxs-lookup"><span data-stu-id="235ab-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="235ab-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="235ab-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="235ab-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="235ab-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="235ab-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="235ab-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="235ab-134">DLL</span><span class="sxs-lookup"><span data-stu-id="235ab-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="235ab-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="235ab-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235ab-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="235ab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235ab-137">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="235ab-137">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="235ab-138">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="235ab-138">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="235ab-139">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="235ab-139">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="235ab-140">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="235ab-140">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="235ab-141">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="235ab-141">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="235ab-142">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="235ab-142">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="235ab-143">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="235ab-143">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="235ab-144">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="235ab-144">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="235ab-145">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="235ab-145">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





