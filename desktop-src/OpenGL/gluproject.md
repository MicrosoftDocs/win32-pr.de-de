---
title: gluproject-Funktion (glu. h)
description: Die Funktion "gluproject" ordnet den Fenster Koordinaten Objekt Koordinaten zu.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluproject-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478024"
---
# <a name="gluproject-function"></a><span data-ttu-id="de3c6-104">gluproject-Funktion</span><span class="sxs-lookup"><span data-stu-id="de3c6-104">gluProject function</span></span>

<span data-ttu-id="de3c6-105">Die Funktion " **gluproject** " ordnet den Fenster Koordinaten Objekt Koordinaten zu.</span><span class="sxs-lookup"><span data-stu-id="de3c6-105">The **gluProject** function maps object coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3c6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="de3c6-106">Syntax</span></span>


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a><span data-ttu-id="de3c6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="de3c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3c6-108">*objX*</span><span class="sxs-lookup"><span data-stu-id="de3c6-108">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-109">Die x-Objekt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="de3c6-109">The x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="de3c6-110">*objy*</span><span class="sxs-lookup"><span data-stu-id="de3c6-110">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-111">Die y-Objekt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="de3c6-111">The y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="de3c6-112">*objz*</span><span class="sxs-lookup"><span data-stu-id="de3c6-112">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-113">Die z-Objekt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="de3c6-113">The z object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="de3c6-114">*modelmatrix*</span><span class="sxs-lookup"><span data-stu-id="de3c6-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-115">Die aktuelle Modelview-Matrix (wie von einem [**glgetdoublev**](glgetdoublev.md) -Befehl).</span><span class="sxs-lookup"><span data-stu-id="de3c6-115">The current modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="de3c6-116">*projmatrix*</span><span class="sxs-lookup"><span data-stu-id="de3c6-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-117">Die aktuelle Projektions Matrix (wie bei einem **glgetdoublev** -Befehl).</span><span class="sxs-lookup"><span data-stu-id="de3c6-117">The current projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="de3c6-118">*Viewport*</span><span class="sxs-lookup"><span data-stu-id="de3c6-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-119">Der aktuelle Viewport (wie bei einem [**glgetintegerv**](glgetintegerv.md) -Befehl).</span><span class="sxs-lookup"><span data-stu-id="de3c6-119">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="de3c6-120">*Winx*</span><span class="sxs-lookup"><span data-stu-id="de3c6-120">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-121">Die berechnete x-Fenster Koordinate.</span><span class="sxs-lookup"><span data-stu-id="de3c6-121">The computed x window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="de3c6-122">*Winy*</span><span class="sxs-lookup"><span data-stu-id="de3c6-122">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-123">Die berechnete y-Fenster Koordinate.</span><span class="sxs-lookup"><span data-stu-id="de3c6-123">The computed y window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="de3c6-124">*Winz*</span><span class="sxs-lookup"><span data-stu-id="de3c6-124">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="de3c6-125">Die berechnete z-Fenster Koordinate.</span><span class="sxs-lookup"><span data-stu-id="de3c6-125">The computed z window coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3c6-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de3c6-126">Return value</span></span>

<span data-ttu-id="de3c6-127">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert "GL \_ true".</span><span class="sxs-lookup"><span data-stu-id="de3c6-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="de3c6-128">Wenn die Funktion fehlschlägt, ist der Rückgabewert "GL \_ false".</span><span class="sxs-lookup"><span data-stu-id="de3c6-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="de3c6-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de3c6-129">Remarks</span></span>

<span data-ttu-id="de3c6-130">Die Funktion " **gluproject** " wandelt die angegebenen Objekt Koordinaten mithilfe von " *modelmatrix*", " *projmatrix*" und " *Viewport*" in Fenster Koordinaten um.</span><span class="sxs-lookup"><span data-stu-id="de3c6-130">The **gluProject** function transforms the specified object coordinates into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="de3c6-131">Das Ergebnis wird in *Winx*, *Winy* und *Winz* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="de3c6-131">The result is stored in *winx*, *winy*, and *winz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="de3c6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de3c6-132">Requirements</span></span>



| <span data-ttu-id="de3c6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de3c6-133">Requirement</span></span> | <span data-ttu-id="de3c6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="de3c6-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="de3c6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de3c6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="de3c6-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de3c6-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="de3c6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de3c6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="de3c6-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de3c6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="de3c6-139">Header</span><span class="sxs-lookup"><span data-stu-id="de3c6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="de3c6-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="de3c6-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="de3c6-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de3c6-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="de3c6-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de3c6-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="de3c6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="de3c6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de3c6-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de3c6-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3c6-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de3c6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3c6-146">**glgetdoublev**</span><span class="sxs-lookup"><span data-stu-id="de3c6-146">**glGetDoublev**</span></span>](glgetdoublev.md)
</dt> <dt>

[<span data-ttu-id="de3c6-147">**glgetintegerv**</span><span class="sxs-lookup"><span data-stu-id="de3c6-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="de3c6-148">**"gluunproject"**</span><span class="sxs-lookup"><span data-stu-id="de3c6-148">**gluUnProject**</span></span>](gluunproject.md)
</dt> </dl>

 

 





