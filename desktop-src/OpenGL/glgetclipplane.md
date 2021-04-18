---
title: glgetclipplane-Funktion (GL. h)
description: Die Funktion "glgetclipplane" gibt die Koeffizienten der angegebenen Clippingebene zurück.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glgetclipplane-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345530"
---
# <a name="glgetclipplane-function"></a><span data-ttu-id="e57ca-104">glgetclipplane-Funktion</span><span class="sxs-lookup"><span data-stu-id="e57ca-104">glGetClipPlane function</span></span>

<span data-ttu-id="e57ca-105">Die Funktion " **glgetclipplane** " gibt die Koeffizienten der angegebenen Clippingebene zurück.</span><span class="sxs-lookup"><span data-stu-id="e57ca-105">The **glGetClipPlane** function returns the coefficients of the specified clipping plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="e57ca-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e57ca-106">Syntax</span></span>


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="e57ca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e57ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e57ca-108">*Wasser*</span><span class="sxs-lookup"><span data-stu-id="e57ca-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="e57ca-109">Eine Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="e57ca-109">A clipping plane.</span></span> <span data-ttu-id="e57ca-110">Die Anzahl der Clippingebenen hängt von der Implementierung ab, es werden jedoch mindestens sechs Clippingebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e57ca-110">The number of clipping planes depends on the implementation, but at least six clipping planes are supported.</span></span> <span data-ttu-id="e57ca-111">Sie werden durch symbolische Namen der Form "GL \_ Clip Plane i" identifiziert, \_ wobei 0 = *i* < GL  \_ Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e57ca-111">They are identified by symbolic names of the form GL\_CLIP\_PLANE *i* where 0 = *i* < GL\_MAX\_CLIP\_PLANES.</span></span>

</dd> <dt>

<span data-ttu-id="e57ca-112">*Gleichung*</span><span class="sxs-lookup"><span data-stu-id="e57ca-112">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="e57ca-113">Gibt vier Werte mit doppelter Genauigkeit zurück, bei denen es sich um die Koeffizienten der ebenengleichung *der Ebenen in* Eye-Koordinaten handelt.</span><span class="sxs-lookup"><span data-stu-id="e57ca-113">Returns four double-precision values that are the coefficients of the plane equation of *plane* in eye coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e57ca-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e57ca-114">Return value</span></span>

<span data-ttu-id="e57ca-115">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e57ca-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e57ca-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e57ca-116">Error codes</span></span>

<span data-ttu-id="e57ca-117">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e57ca-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e57ca-118">Name</span><span class="sxs-lookup"><span data-stu-id="e57ca-118">Name</span></span>                                                                                                  | <span data-ttu-id="e57ca-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e57ca-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e57ca-120"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e57ca-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e57ca-121">die *Ebene* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="e57ca-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="e57ca-122"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="e57ca-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e57ca-123">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e57ca-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e57ca-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e57ca-124">Remarks</span></span>

<span data-ttu-id="e57ca-125">Die Funktion " **glgetclipplane** " gibt die vier Koeffizienten der ebenengleichung für die *Ebene* in *Gleichung* zurück.</span><span class="sxs-lookup"><span data-stu-id="e57ca-125">The **glGetClipPlane** function returns in *equation* the four coefficients of the plane equation for *plane*.</span></span>

<span data-ttu-id="e57ca-126">Es ist immer der Fall, dass GL \_ Clip \_ Plane *i* = GL \_ Clip \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="e57ca-126">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="e57ca-127">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt der *Gleichung* vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="e57ca-127">If an error is generated, no change is made to the contents of *equation*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e57ca-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e57ca-128">Requirements</span></span>



| <span data-ttu-id="e57ca-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e57ca-129">Requirement</span></span> | <span data-ttu-id="e57ca-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e57ca-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e57ca-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e57ca-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e57ca-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e57ca-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e57ca-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e57ca-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e57ca-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e57ca-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e57ca-135">Header</span><span class="sxs-lookup"><span data-stu-id="e57ca-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e57ca-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e57ca-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e57ca-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e57ca-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e57ca-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e57ca-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e57ca-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e57ca-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e57ca-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e57ca-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e57ca-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e57ca-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e57ca-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e57ca-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e57ca-143">**glclipplane**</span><span class="sxs-lookup"><span data-stu-id="e57ca-143">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="e57ca-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e57ca-144">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





