---
title: glTexCoord2d-Funktion (GL. h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord2d-Funktion (GL. h)
ms.assetid: 624d566f-72ae-4a7d-adad-5fcfee5b5aca
keywords:
- glTexCoord2d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825df8eb8adbfca08b11620d74928284a613780b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363086"
---
# <a name="gltexcoord2d-function"></a><span data-ttu-id="ff292-105">glTexCoord2d-Funktion</span><span class="sxs-lookup"><span data-stu-id="ff292-105">glTexCoord2d function</span></span>

<span data-ttu-id="ff292-106">Legt die aktuellen Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="ff292-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff292-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff292-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2d(
   GLdouble s,
   GLdouble t
);
```



## <a name="parameters"></a><span data-ttu-id="ff292-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff292-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff292-109">*s*</span><span class="sxs-lookup"><span data-stu-id="ff292-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="ff292-110">Die s-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="ff292-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="ff292-111">*t*</span><span class="sxs-lookup"><span data-stu-id="ff292-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="ff292-112">Die t-Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="ff292-112">The t texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff292-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff292-113">Return value</span></span>

<span data-ttu-id="ff292-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ff292-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff292-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff292-115">Remarks</span></span>

<span data-ttu-id="ff292-116">Die [**gltexcoord**](gltexcoord-functions.md) -Funktion legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygon Scheitel Punkten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ff292-116">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="ff292-117">Die **gltexcoord** -Funktion gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="ff292-117">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="ff292-118">Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. bei einem glTexCoord2-Aufrufsatz werden diese auf (s, t, 0, 1) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ff292-118">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="ff292-119">Entsprechend gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="ff292-119">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="ff292-120">Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ff292-120">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="ff292-121">Vor allem können Sie "gltexcoord" zwischen einem Aufrufen von " [**glBegin**](glbegin.md) " und dem entsprechenden " [**glEnd**](glend.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ff292-121">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="ff292-122">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexcoord** ab:</span><span class="sxs-lookup"><span data-stu-id="ff292-122">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="ff292-123">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="ff292-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="ff292-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff292-124">Requirements</span></span>



| <span data-ttu-id="ff292-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff292-125">Requirement</span></span> | <span data-ttu-id="ff292-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ff292-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff292-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff292-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ff292-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff292-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ff292-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff292-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ff292-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff292-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff292-131">Header</span><span class="sxs-lookup"><span data-stu-id="ff292-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff292-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff292-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ff292-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff292-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff292-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff292-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff292-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ff292-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff292-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff292-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff292-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff292-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff292-138">glVertex</span><span class="sxs-lookup"><span data-stu-id="ff292-138">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





