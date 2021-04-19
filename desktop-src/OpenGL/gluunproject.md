---
title: gluunproject-Funktion (glu. h)
description: Die Funktion "gluunproject" ordnet den Objekt Koordinaten Fenster Koordinaten zu.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- gluunproject-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345928"
---
# <a name="gluunproject-function"></a><span data-ttu-id="cfb5f-104">gluunproject-Funktion</span><span class="sxs-lookup"><span data-stu-id="cfb5f-104">gluUnProject function</span></span>

<span data-ttu-id="cfb5f-105">Die Funktion " **gluunproject** " ordnet den Objekt Koordinaten Fenster Koordinaten zu.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-105">The **gluUnProject** function maps window coordinates to object coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb5f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfb5f-106">Syntax</span></span>


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a><span data-ttu-id="cfb5f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfb5f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb5f-108">*Winx*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-108">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-109">Die zuzuordnende x-Fenster Koordinate.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-109">The x window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="cfb5f-110">*Winy*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-110">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-111">Die zuzuordnende y-Fenster Koordinate.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-111">The y window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="cfb5f-112">*Winz*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-112">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-113">Die zu zugeordnete z-Fenster Koordinate.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-113">The z window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="cfb5f-114">*modelmatrix*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-115">Die Modelview-Matrix (wie bei einem [**glgetdoublev**](glgetdoublev.md) -Befehl).</span><span class="sxs-lookup"><span data-stu-id="cfb5f-115">The modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="cfb5f-116">*projmatrix*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-117">Die Projektions Matrix (wie bei einem **glgetdoublev** -Befehl).</span><span class="sxs-lookup"><span data-stu-id="cfb5f-117">The projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="cfb5f-118">*Viewport*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-119">Der Viewport (wie bei einem [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) -Befehl).</span><span class="sxs-lookup"><span data-stu-id="cfb5f-119">The viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="cfb5f-120">*objX*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-120">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-121">Die berechnete x-Objekt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-121">The computed x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cfb5f-122">*objy*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-122">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-123">Die berechnete y-Objekt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-123">The computed y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cfb5f-124">*objz*</span><span class="sxs-lookup"><span data-stu-id="cfb5f-124">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb5f-125">Die berechnete z-Objekt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-125">The computed z object coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb5f-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfb5f-126">Return value</span></span>

<span data-ttu-id="cfb5f-127">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert "GL \_ true".</span><span class="sxs-lookup"><span data-stu-id="cfb5f-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="cfb5f-128">Wenn die Funktion fehlschlägt, ist der Rückgabewert "GL \_ false".</span><span class="sxs-lookup"><span data-stu-id="cfb5f-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb5f-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfb5f-129">Remarks</span></span>

<span data-ttu-id="cfb5f-130">Die Funktion " **gluunproject** " ordnet die angegebenen Fenster Koordinaten mithilfe von " *modelmatrix*", " *projmatrix*" und " *Viewport*" den Objekt Koordinaten zu.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-130">The **gluUnProject** function maps the specified window coordinates into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="cfb5f-131">Das Ergebnis wird in *objX*, *objy* und *objz* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cfb5f-131">The result is stored in *objx*, *objy*, and *objz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb5f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfb5f-132">Requirements</span></span>



| <span data-ttu-id="cfb5f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfb5f-133">Requirement</span></span> | <span data-ttu-id="cfb5f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb5f-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb5f-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfb5f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb5f-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfb5f-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cfb5f-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfb5f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb5f-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfb5f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cfb5f-139">Header</span><span class="sxs-lookup"><span data-stu-id="cfb5f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb5f-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb5f-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cfb5f-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cfb5f-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="cfb5f-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfb5f-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cfb5f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cfb5f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfb5f-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfb5f-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb5f-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfb5f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb5f-146">**glget**</span><span class="sxs-lookup"><span data-stu-id="cfb5f-146">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="cfb5f-147">**glgetdoublev**</span><span class="sxs-lookup"><span data-stu-id="cfb5f-147">**glGetDoublev**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="cfb5f-148">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="cfb5f-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="cfb5f-149">**gluproject**</span><span class="sxs-lookup"><span data-stu-id="cfb5f-149">**gluProject**</span></span>](gluproject.md)
</dt> </dl>

 

 





