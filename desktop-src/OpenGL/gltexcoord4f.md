---
title: glTexCoord4f-Funktion (GL. h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord4f-Funktion (GL. h)
ms.assetid: d2c190cd-3af2-425b-985b-0c66be11ef28
keywords:
- glTexCoord4f-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6720effb93f233338b3e8dfbce44f4651a1061b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357205"
---
# <a name="gltexcoord4f-function"></a><span data-ttu-id="1baaa-105">glTexCoord4f-Funktion</span><span class="sxs-lookup"><span data-stu-id="1baaa-105">glTexCoord4f function</span></span>

<span data-ttu-id="1baaa-106">Legt die aktuellen Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="1baaa-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="1baaa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1baaa-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4f(
   GLfloat s,
   GLfloat t,
   GLfloat r,
   GLfloat q
);
```



## <a name="parameters"></a><span data-ttu-id="1baaa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1baaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1baaa-109">*s*</span><span class="sxs-lookup"><span data-stu-id="1baaa-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="1baaa-110">Die s-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="1baaa-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="1baaa-111">*t*</span><span class="sxs-lookup"><span data-stu-id="1baaa-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="1baaa-112">Die t-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="1baaa-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="1baaa-113">*r*</span><span class="sxs-lookup"><span data-stu-id="1baaa-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="1baaa-114">Die r-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="1baaa-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="1baaa-115">*Q1*</span><span class="sxs-lookup"><span data-stu-id="1baaa-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="1baaa-116">Die q-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="1baaa-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1baaa-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1baaa-117">Return value</span></span>

<span data-ttu-id="1baaa-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1baaa-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1baaa-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1baaa-119">Remarks</span></span>

<span data-ttu-id="1baaa-120">Die [**gltexcoord**](gltexcoord-functions.md) -Funktion legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygon Scheitel Punkten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1baaa-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="1baaa-121">Die **gltexcoord** -Funktion gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="1baaa-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="1baaa-122">Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. bei einem glTexCoord2-Aufrufsatz werden diese auf (s, t, 0, 1) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1baaa-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="1baaa-123">Entsprechend gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="1baaa-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="1baaa-124">Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1baaa-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="1baaa-125">Vor allem können Sie "gltexcoord" zwischen einem Aufrufen von " [**glBegin**](glbegin.md) " und dem entsprechenden " [**glEnd**](glend.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1baaa-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="1baaa-126">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexcoord** ab:</span><span class="sxs-lookup"><span data-stu-id="1baaa-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="1baaa-127">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="1baaa-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="1baaa-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1baaa-128">Requirements</span></span>



| <span data-ttu-id="1baaa-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1baaa-129">Requirement</span></span> | <span data-ttu-id="1baaa-130">Wert</span><span class="sxs-lookup"><span data-stu-id="1baaa-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1baaa-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1baaa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1baaa-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1baaa-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1baaa-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1baaa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1baaa-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1baaa-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1baaa-135">Header</span><span class="sxs-lookup"><span data-stu-id="1baaa-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1baaa-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1baaa-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1baaa-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1baaa-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="1baaa-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1baaa-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1baaa-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1baaa-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1baaa-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1baaa-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1baaa-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1baaa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1baaa-142">glVertex</span><span class="sxs-lookup"><span data-stu-id="1baaa-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





