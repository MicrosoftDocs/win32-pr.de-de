---
title: glTexCoord3s-Funktion (GL. h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord3s-Funktion (GL. h)
ms.assetid: 0698c7fe-3a1a-4713-a72b-17d81840251b
keywords:
- glTexCoord3s-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057f04fd2a811e7da34c7797dd4ca61ad9b5ff69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870003"
---
# <a name="gltexcoord3s-function"></a><span data-ttu-id="9ce0a-105">glTexCoord3s-Funktion</span><span class="sxs-lookup"><span data-stu-id="9ce0a-105">glTexCoord3s function</span></span>

<span data-ttu-id="9ce0a-106">Legt die aktuellen Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce0a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ce0a-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3s(
   GLshort s,
   GLshort t,
   GLshort r
);
```



## <a name="parameters"></a><span data-ttu-id="9ce0a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ce0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ce0a-109">*s*</span><span class="sxs-lookup"><span data-stu-id="9ce0a-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce0a-110">Die s-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9ce0a-111">*t*</span><span class="sxs-lookup"><span data-stu-id="9ce0a-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce0a-112">Die t-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9ce0a-113">*r*</span><span class="sxs-lookup"><span data-stu-id="9ce0a-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce0a-114">Die r-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-114">The r texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ce0a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ce0a-115">Return value</span></span>

<span data-ttu-id="9ce0a-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ce0a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ce0a-117">Remarks</span></span>

<span data-ttu-id="9ce0a-118">Die [**gltexcoord**](gltexcoord-functions.md) -Funktion legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygon Scheitel Punkten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-118">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="9ce0a-119">Die **gltexcoord** -Funktion gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-119">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="9ce0a-120">Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. bei einem glTexCoord2-Aufrufsatz werden diese auf (s, t, 0, 1) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-120">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="9ce0a-121">Entsprechend gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="9ce0a-121">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="9ce0a-122">Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-122">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="9ce0a-123">Vor allem können Sie "gltexcoord" zwischen einem Aufrufen von " [**glBegin**](glbegin.md) " und dem entsprechenden " [**glEnd**](glend.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9ce0a-123">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="9ce0a-124">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexcoord** ab:</span><span class="sxs-lookup"><span data-stu-id="9ce0a-124">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="9ce0a-125">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="9ce0a-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce0a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ce0a-126">Requirements</span></span>



| <span data-ttu-id="9ce0a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ce0a-127">Requirement</span></span> | <span data-ttu-id="9ce0a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9ce0a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce0a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ce0a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce0a-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ce0a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9ce0a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ce0a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce0a-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ce0a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ce0a-133">Header</span><span class="sxs-lookup"><span data-stu-id="9ce0a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ce0a-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce0a-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9ce0a-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9ce0a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ce0a-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ce0a-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ce0a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9ce0a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ce0a-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ce0a-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce0a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ce0a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce0a-140">glVertex</span><span class="sxs-lookup"><span data-stu-id="9ce0a-140">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





