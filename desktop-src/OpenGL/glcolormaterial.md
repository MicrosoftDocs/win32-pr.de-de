---
title: glcolormaterial-Funktion (GL. h)
description: Die glcolormaterial-Funktion bewirkt, dass die aktuelle Farbe mit einer Material Farbe nachverfolgt wird.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glcolormaterial-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391994"
---
# <a name="glcolormaterial-function"></a><span data-ttu-id="4b33a-104">glcolormaterial-Funktion</span><span class="sxs-lookup"><span data-stu-id="4b33a-104">glColorMaterial function</span></span>

<span data-ttu-id="4b33a-105">Die **glcolormaterial** -Funktion bewirkt, dass die aktuelle Farbe mit einer Material Farbe nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="4b33a-105">The **glColorMaterial** function causes a material color to track the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b33a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b33a-106">Syntax</span></span>


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="4b33a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b33a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b33a-108">*mit*</span><span class="sxs-lookup"><span data-stu-id="4b33a-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="4b33a-109">Gibt an, ob die Vorder-, Hintergrund-oder beide Vorder-und Hintergrundmaterial Parameter die aktuelle Farbe verfolgen sollen.</span><span class="sxs-lookup"><span data-stu-id="4b33a-109">Specifies whether front, back, or both front and back material parameters should track the current color.</span></span> <span data-ttu-id="4b33a-110">Akzeptierte Werte sind GL \_ Front, GL \_ Back und GL \_ Front \_ und \_ Back.</span><span class="sxs-lookup"><span data-stu-id="4b33a-110">Accepted values are GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK.</span></span> <span data-ttu-id="4b33a-111">Der Standardwert ist GL \_ Front \_ und \_ Back.</span><span class="sxs-lookup"><span data-stu-id="4b33a-111">The default value is GL\_FRONT\_AND\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="4b33a-112">*mode*</span><span class="sxs-lookup"><span data-stu-id="4b33a-112">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="4b33a-113">Gibt an, welche von mehreren Materialparametern die aktuelle Farbe nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="4b33a-113">Specifies which of several material parameters track the current color.</span></span> <span data-ttu-id="4b33a-114">Akzeptierte Werte sind GL \_ -Ausgabe, GL \_ Ambient, GL \_ diffus, GL \_ specarität und GL \_ Ambient \_ und \_ diffuse.</span><span class="sxs-lookup"><span data-stu-id="4b33a-114">Accepted values are GL\_EMISSION, GL\_AMBIENT, GL\_DIFFUSE, GL\_SPECULAR, and GL\_AMBIENT\_AND\_DIFFUSE.</span></span> <span data-ttu-id="4b33a-115">Der Standardwert ist "GL \_ AMBIENT" und "diffuse" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b33a-115">The default value is GL\_AMBIENT\_AND\_DIFFUSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b33a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b33a-116">Return value</span></span>

<span data-ttu-id="4b33a-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4b33a-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b33a-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4b33a-118">Error codes</span></span>

<span data-ttu-id="4b33a-119">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4b33a-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4b33a-120">Name</span><span class="sxs-lookup"><span data-stu-id="4b33a-120">Name</span></span>                                                                                                  | <span data-ttu-id="4b33a-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4b33a-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b33a-122"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4b33a-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4b33a-123">der *Gesichts* -oder *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="4b33a-123">*face* or *mode* was not an accepted value.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="4b33a-124"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="4b33a-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4b33a-125">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4b33a-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4b33a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b33a-126">Remarks</span></span>

<span data-ttu-id="4b33a-127">Die **glcolormaterial** -Funktion gibt an, welche Materialparameter die aktuelle Farbe verfolgen.</span><span class="sxs-lookup"><span data-stu-id="4b33a-127">The **glColorMaterial** function specifies which material parameters track the current color.</span></span> <span data-ttu-id="4b33a-128">Wenn Sie das GL- \_ Farb \_ Material aktivieren, wird für jedes Material oder jedes Material, das durch das *Gesicht* angegeben wird, der Materialparameter oder die Parameter, die vom- *Modus* angegeben werden, die aktuelle Farbe jederzeit nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="4b33a-128">When you enable GL\_COLOR\_MATERIAL, for each of the material or materials specified by *face*, the material parameter or parameters specified by *mode* track the current color at all times.</span></span> <span data-ttu-id="4b33a-129">Aktivieren und deaktivieren \_ Sie das GL-Farb \_ Material mit den Funktionen [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md), die Sie mit dem GL- \_ Farb \_ Material als Argument aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4b33a-129">Enable and disable GL\_COLOR\_MATERIAL with the functions [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), which you call with GL\_COLOR\_MATERIAL as their argument.</span></span> <span data-ttu-id="4b33a-130">Standardmäßig ist das GL- \_ Farb \_ Material deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4b33a-130">By default, GL\_COLOR\_MATERIAL is disabled.</span></span>

<span data-ttu-id="4b33a-131">Mit **glcolormaterial** können Sie eine Teilmenge der Materialparameter für jeden Scheitelpunkt mithilfe der Funktion " [**glcolor**](glcolor-functions.md) " ändern, ohne " [**glmaterial**](glmaterial-functions.md)" aufrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="4b33a-131">With **glColorMaterial**, you can change a subset of material parameters for each vertex using only the [**glColor**](glcolor-functions.md) function, without calling [**glMaterial**](glmaterial-functions.md).</span></span> <span data-ttu-id="4b33a-132">Wenn Sie nur eine solche Teilmenge von Parametern für jeden Scheitelpunkt angeben, ist es besser, dies mit **glcolormaterial** zu tun, als bei **glmaterial**.</span><span class="sxs-lookup"><span data-stu-id="4b33a-132">If you are going to specify only such a subset of parameters for each vertex, it is better to do so with **glColorMaterial** than with **glMaterial**.</span></span>

<span data-ttu-id="4b33a-133">Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glcolormaterial** ab:</span><span class="sxs-lookup"><span data-stu-id="4b33a-133">The following functions retrieve information related to **glColorMaterial**:</span></span>

<span data-ttu-id="4b33a-134">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Color \_ Material \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="4b33a-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_MATERIAL\_PARAMETER</span></span>

<span data-ttu-id="4b33a-135">**glget** mit dem Argument GL \_ Color \_ Material \_ Face</span><span class="sxs-lookup"><span data-stu-id="4b33a-135">**glGet** with argument GL\_COLOR\_MATERIAL\_FACE</span></span>

<span data-ttu-id="4b33a-136">[**glisenabled**](glisenabled.md) mit dem Argument "GL \_ Color \_ Material"</span><span class="sxs-lookup"><span data-stu-id="4b33a-136">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_MATERIAL</span></span>

## <a name="requirements"></a><span data-ttu-id="4b33a-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b33a-137">Requirements</span></span>



| <span data-ttu-id="4b33a-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b33a-138">Requirement</span></span> | <span data-ttu-id="4b33a-139">Wert</span><span class="sxs-lookup"><span data-stu-id="4b33a-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b33a-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b33a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4b33a-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b33a-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4b33a-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b33a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4b33a-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b33a-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b33a-144">Header</span><span class="sxs-lookup"><span data-stu-id="4b33a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b33a-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b33a-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4b33a-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b33a-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b33a-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b33a-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4b33a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4b33a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b33a-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b33a-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b33a-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b33a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b33a-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4b33a-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4b33a-152">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="4b33a-152">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="4b33a-153">**gldeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="4b33a-153">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="4b33a-154">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="4b33a-154">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="4b33a-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4b33a-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4b33a-156">**glget**</span><span class="sxs-lookup"><span data-stu-id="4b33a-156">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4b33a-157">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="4b33a-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="4b33a-158">**gllight**</span><span class="sxs-lookup"><span data-stu-id="4b33a-158">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="4b33a-159">**gllightmodel**</span><span class="sxs-lookup"><span data-stu-id="4b33a-159">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="4b33a-160">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="4b33a-160">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





