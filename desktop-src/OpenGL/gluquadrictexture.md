---
title: gluquadrictexture-Funktion (glu. h)
description: Die Funktion "gluquadrictexture" gibt an, ob viercs texturiert werden sollen.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluquadrictexture-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104930"
---
# <a name="gluquadrictexture-function"></a><span data-ttu-id="d276b-104">gluquadrictexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="d276b-104">gluQuadricTexture function</span></span>

<span data-ttu-id="d276b-105">Die Funktion " **gluquadrictexture** " gibt an, ob viercs texturiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d276b-105">The **gluQuadricTexture** function specifies whether quadrics are to be textured.</span></span>

## <a name="syntax"></a><span data-ttu-id="d276b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d276b-106">Syntax</span></span>


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a><span data-ttu-id="d276b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d276b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d276b-108">*quadobject*</span><span class="sxs-lookup"><span data-stu-id="d276b-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="d276b-109">Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="d276b-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d276b-110">*texturecoords*</span><span class="sxs-lookup"><span data-stu-id="d276b-110">*textureCoords*</span></span> 
</dt> <dd>

<span data-ttu-id="d276b-111">Ein Flag, das angibt, ob Texturkoordinaten generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d276b-111">A flag indicating whether texture coordinates are to be generated.</span></span> <span data-ttu-id="d276b-112">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="d276b-112">The following values are valid.</span></span>



| <span data-ttu-id="d276b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d276b-113">Value</span></span>                                                                                                                                          | <span data-ttu-id="d276b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d276b-114">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <span data-ttu-id="d276b-115"><dt>**GL \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="d276b-115"><dt>**GL\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="d276b-116">Texturkoordinaten generieren.</span><span class="sxs-lookup"><span data-stu-id="d276b-116">Generate texture coordinates.</span></span><br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <span data-ttu-id="d276b-117"><dt>**GL \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d276b-117"><dt>**GL\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d276b-118">Keine Texturkoordinaten generieren.</span><span class="sxs-lookup"><span data-stu-id="d276b-118">Do not generate texture coordinates.</span></span> <span data-ttu-id="d276b-119">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="d276b-119">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d276b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d276b-120">Return value</span></span>

<span data-ttu-id="d276b-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d276b-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d276b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d276b-122">Remarks</span></span>

<span data-ttu-id="d276b-123">Die Funktion " **gluquadrictexture** " gibt an, ob Texturkoordinaten für viercs generiert werden sollen, die mit **quadobject** gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="d276b-123">The **gluQuadricTexture** function specifies whether texture coordinates are to be generated for quadrics rendered with **quadObject**.</span></span>

<span data-ttu-id="d276b-124">Die Art und Weise, in der Texturkoordinaten generiert werden, hängt von dem gerenderten Quadric ab.</span><span class="sxs-lookup"><span data-stu-id="d276b-124">The manner in which texture coordinates are generated depends upon the specific quadric rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="d276b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d276b-125">Requirements</span></span>



| <span data-ttu-id="d276b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d276b-126">Requirement</span></span> | <span data-ttu-id="d276b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d276b-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d276b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d276b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d276b-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d276b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d276b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d276b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d276b-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d276b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d276b-132">Header</span><span class="sxs-lookup"><span data-stu-id="d276b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d276b-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d276b-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d276b-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d276b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d276b-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d276b-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d276b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d276b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d276b-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d276b-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d276b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d276b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d276b-139">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="d276b-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="d276b-140">**gluquadricdrawstyle**</span><span class="sxs-lookup"><span data-stu-id="d276b-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="d276b-141">**gluquadricnormals**</span><span class="sxs-lookup"><span data-stu-id="d276b-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> </dl>

 

 





