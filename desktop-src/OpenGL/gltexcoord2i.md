---
title: glTexCoord2i-Funktion (GL. h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord2i-Funktion (GL. h)
ms.assetid: 7a5ff9a7-8dcd-47a0-868c-3909e011a592
keywords:
- glTexCoord2i-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa4d710f49d55e8aa0379bfc83f79f877d3cc906
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363937"
---
# <a name="gltexcoord2i-function"></a><span data-ttu-id="334b6-105">glTexCoord2i-Funktion</span><span class="sxs-lookup"><span data-stu-id="334b6-105">glTexCoord2i function</span></span>

<span data-ttu-id="334b6-106">Legt die aktuellen Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="334b6-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="334b6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="334b6-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2i(
   GLint s,
   GLint t
);
```



## <a name="parameters"></a><span data-ttu-id="334b6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="334b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="334b6-109">*s*</span><span class="sxs-lookup"><span data-stu-id="334b6-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="334b6-110">Die s-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="334b6-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="334b6-111">*t*</span><span class="sxs-lookup"><span data-stu-id="334b6-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="334b6-112">Die t-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="334b6-112">The t texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="334b6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="334b6-113">Return value</span></span>

<span data-ttu-id="334b6-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="334b6-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="334b6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="334b6-115">Remarks</span></span>

<span data-ttu-id="334b6-116">Die [**gltexcoord**](gltexcoord-functions.md) -Funktion legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygon Scheitel Punkten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="334b6-116">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="334b6-117">Die **gltexcoord** -Funktion gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="334b6-117">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="334b6-118">Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. bei einem glTexCoord2-Aufrufsatz werden diese auf (s, t, 0, 1) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="334b6-118">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="334b6-119">Entsprechend gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="334b6-119">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="334b6-120">Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="334b6-120">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="334b6-121">Vor allem können Sie "gltexcoord" zwischen einem Aufrufen von " [**glBegin**](glbegin.md) " und dem entsprechenden " [**glEnd**](glend.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="334b6-121">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="334b6-122">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexcoord** ab:</span><span class="sxs-lookup"><span data-stu-id="334b6-122">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="334b6-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="334b6-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="334b6-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="334b6-124">Requirements</span></span>



| <span data-ttu-id="334b6-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="334b6-125">Requirement</span></span> | <span data-ttu-id="334b6-126">Wert</span><span class="sxs-lookup"><span data-stu-id="334b6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="334b6-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="334b6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="334b6-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="334b6-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="334b6-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="334b6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="334b6-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="334b6-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="334b6-131">Header</span><span class="sxs-lookup"><span data-stu-id="334b6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="334b6-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="334b6-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="334b6-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="334b6-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="334b6-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="334b6-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="334b6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="334b6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="334b6-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="334b6-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="334b6-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="334b6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="334b6-138">glVertex</span><span class="sxs-lookup"><span data-stu-id="334b6-138">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





