---
title: glTexCoord4i-Funktion (GL. h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord4i-Funktion (GL. h)
ms.assetid: b2b49102-5129-49cc-9043-22ba46fbf08f
keywords:
- glTexCoord4i-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ecdcddc7a62a2cce4adf595321c72dd877aa69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366601"
---
# <a name="gltexcoord4i-function"></a><span data-ttu-id="7d888-105">glTexCoord4i-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d888-105">glTexCoord4i function</span></span>

<span data-ttu-id="7d888-106">Legt die aktuellen Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="7d888-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d888-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d888-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4i(
   GLint s,
   GLint t,
   GLint r,
   GLint q
);
```



## <a name="parameters"></a><span data-ttu-id="7d888-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d888-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d888-109">*s*</span><span class="sxs-lookup"><span data-stu-id="7d888-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="7d888-110">Die s-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="7d888-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="7d888-111">*t*</span><span class="sxs-lookup"><span data-stu-id="7d888-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="7d888-112">Die t-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="7d888-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="7d888-113">*r*</span><span class="sxs-lookup"><span data-stu-id="7d888-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="7d888-114">Die r-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="7d888-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="7d888-115">*Q1*</span><span class="sxs-lookup"><span data-stu-id="7d888-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="7d888-116">Die q-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="7d888-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d888-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d888-117">Return value</span></span>

<span data-ttu-id="7d888-118">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7d888-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d888-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d888-119">Remarks</span></span>

<span data-ttu-id="7d888-120">Die [**gltexcoord**](gltexcoord-functions.md) -Funktion legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygon Scheitel Punkten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7d888-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="7d888-121">Die **gltexcoord** -Funktion gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="7d888-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="7d888-122">Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. bei einem glTexCoord2-Aufrufsatz werden diese auf (s, t, 0, 1) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7d888-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="7d888-123">Entsprechend gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="7d888-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="7d888-124">Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7d888-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="7d888-125">Vor allem können Sie "gltexcoord" zwischen einem Aufrufen von " [**glBegin**](glbegin.md) " und dem entsprechenden " [**glEnd**](glend.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7d888-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="7d888-126">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexcoord** ab:</span><span class="sxs-lookup"><span data-stu-id="7d888-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="7d888-127">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="7d888-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="7d888-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d888-128">Requirements</span></span>



| <span data-ttu-id="7d888-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d888-129">Requirement</span></span> | <span data-ttu-id="7d888-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7d888-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d888-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d888-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7d888-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d888-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7d888-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d888-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7d888-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d888-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7d888-135">Header</span><span class="sxs-lookup"><span data-stu-id="7d888-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d888-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d888-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7d888-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d888-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="7d888-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d888-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d888-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7d888-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d888-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d888-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d888-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d888-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d888-142">glVertex</span><span class="sxs-lookup"><span data-stu-id="7d888-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





