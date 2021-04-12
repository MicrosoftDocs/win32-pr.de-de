---
title: cglTexCoord3f-Funktion (GL. h)
description: Legt die aktuellen Texturkoordinaten fest. | cglTexCoord3f-Funktion (GL. h)
ms.assetid: 5ff078bb-040f-47c0-9051-69cde14ba259
keywords:
- glTexCoord3f-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2667b3208b0c8b6c9c6bc1a25dd2a63686f8ddaa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352789"
---
# <a name="cgltexcoord3f-function"></a><span data-ttu-id="54228-105">cglTexCoord3f-Funktion</span><span class="sxs-lookup"><span data-stu-id="54228-105">cglTexCoord3f function</span></span>

<span data-ttu-id="54228-106">Legt die aktuellen Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="54228-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="54228-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="54228-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3f(
   GLfloat s,
   GLfloat t,
   GLfloat r
);
```



## <a name="parameters"></a><span data-ttu-id="54228-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="54228-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54228-109">*s*</span><span class="sxs-lookup"><span data-stu-id="54228-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="54228-110">Die s-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="54228-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="54228-111">*t*</span><span class="sxs-lookup"><span data-stu-id="54228-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="54228-112">Die t-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="54228-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="54228-113">*r*</span><span class="sxs-lookup"><span data-stu-id="54228-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="54228-114">Die r-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="54228-114">The r texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54228-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54228-115">Return value</span></span>

<span data-ttu-id="54228-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="54228-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54228-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54228-117">Remarks</span></span>

<span data-ttu-id="54228-118">Die [**gltexcoord**](gltexcoord-functions.md) -Funktion legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygon Scheitel Punkten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="54228-118">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="54228-119">Die **gltexcoord** -Funktion gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="54228-119">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="54228-120">Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. bei einem glTexCoord2-Aufrufsatz werden diese auf (s, t, 0, 1) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54228-120">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="54228-121">Entsprechend gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="54228-121">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="54228-122">Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="54228-122">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="54228-123">Vor allem können Sie "gltexcoord" zwischen einem Aufrufen von " [**glBegin**](glbegin.md) " und dem entsprechenden " [**glEnd**](glend.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="54228-123">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="54228-124">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexcoord** ab:</span><span class="sxs-lookup"><span data-stu-id="54228-124">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="54228-125">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="54228-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="54228-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54228-126">Requirements</span></span>



| <span data-ttu-id="54228-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54228-127">Requirement</span></span> | <span data-ttu-id="54228-128">Wert</span><span class="sxs-lookup"><span data-stu-id="54228-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54228-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54228-129">Minimum supported client</span></span><br/> | <span data-ttu-id="54228-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54228-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="54228-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54228-131">Minimum supported server</span></span><br/> | <span data-ttu-id="54228-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54228-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54228-133">Header</span><span class="sxs-lookup"><span data-stu-id="54228-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="54228-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="54228-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="54228-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54228-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="54228-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54228-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="54228-137">DLL</span><span class="sxs-lookup"><span data-stu-id="54228-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54228-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54228-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54228-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54228-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54228-140">glVertex</span><span class="sxs-lookup"><span data-stu-id="54228-140">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





