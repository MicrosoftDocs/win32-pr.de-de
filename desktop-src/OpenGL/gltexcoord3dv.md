---
title: glTexCoord3dv-Funktion (GL. h)
description: Legt die aktuellen Texturkoordinaten fest. | glTexCoord3dv-Funktion (GL. h)
ms.assetid: 410f49d6-7950-4940-a377-d62ca2bd5db7
keywords:
- glTexCoord3dv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4007e6a524075fc7c091cfc3c6e01044aeae3c22
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869843"
---
# <a name="gltexcoord3dv-function"></a><span data-ttu-id="a6c4a-105">glTexCoord3dv-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6c4a-105">glTexCoord3dv function</span></span>

<span data-ttu-id="a6c4a-106">Legt die aktuellen Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="a6c4a-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6c4a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6c4a-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="a6c4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6c4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6c4a-109">*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="a6c4a-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="a6c4a-110">Ein Zeiger auf ein Array von drei Elementen, das wiederum die s-, t-und r-Texturkoordinaten angibt.</span><span class="sxs-lookup"><span data-stu-id="a6c4a-110">A pointer to an array of three elements, which in turn specifies the s, t, and r texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6c4a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6c4a-111">Return value</span></span>

<span data-ttu-id="a6c4a-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a6c4a-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6c4a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6c4a-113">Remarks</span></span>

<span data-ttu-id="a6c4a-114">Die [**gltexcoord**](gltexcoord-functions.md) -Funktion legt die aktuellen Texturkoordinaten fest, die Teil der Daten sind, die Polygon Scheitel Punkten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a6c4a-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="a6c4a-115">Die **gltexcoord** -Funktion gibt Texturkoordinaten in einer, zwei, drei oder vier Dimensionen an.</span><span class="sxs-lookup"><span data-stu-id="a6c4a-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="a6c4a-116">Die glTexCoord1-Funktion legt die aktuellen Texturkoordinaten auf (s, 0, 0, 1) fest. bei einem glTexCoord2-Aufrufsatz werden diese auf (s, t, 0, 1) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a6c4a-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="a6c4a-117">Entsprechend gibt glTexCoord3 die Texturkoordinaten als (s, t, r, 1) an, und glTexCoord4 definiert alle vier Komponenten explizit als (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="a6c4a-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="a6c4a-118">Sie können die aktuellen Texturkoordinaten jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a6c4a-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="a6c4a-119">Vor allem können Sie "gltexcoord" zwischen einem Aufrufen von " [**glBegin**](glbegin.md) " und dem entsprechenden " [**glEnd**](glend.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a6c4a-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="a6c4a-120">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexcoord** ab:</span><span class="sxs-lookup"><span data-stu-id="a6c4a-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="a6c4a-121">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Textur \_ CoOrds</span><span class="sxs-lookup"><span data-stu-id="a6c4a-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="a6c4a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6c4a-122">Requirements</span></span>



| <span data-ttu-id="a6c4a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6c4a-123">Requirement</span></span> | <span data-ttu-id="a6c4a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a6c4a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6c4a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6c4a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a6c4a-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6c4a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a6c4a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6c4a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a6c4a-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6c4a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a6c4a-129">Header</span><span class="sxs-lookup"><span data-stu-id="a6c4a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6c4a-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6c4a-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a6c4a-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6c4a-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6c4a-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6c4a-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a6c4a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a6c4a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6c4a-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6c4a-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6c4a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6c4a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6c4a-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="a6c4a-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





