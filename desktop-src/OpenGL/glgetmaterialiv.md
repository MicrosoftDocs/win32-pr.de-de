---
title: glgetmaterialiv-Funktion (GL. h)
description: Die Funktionen "glgetmaterialfv" und "glgetmaterialiv" geben Materialparameter zurück. | glgetmaterialiv-Funktion (GL. h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- glgetmaterialiv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f09e1a315d4929ebb92f3b0e59ed6762a7fe4b35
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106370375"
---
# <a name="glgetmaterialiv-function"></a><span data-ttu-id="3d6da-105">glgetmaterialiv-Funktion</span><span class="sxs-lookup"><span data-stu-id="3d6da-105">glGetMaterialiv function</span></span>

<span data-ttu-id="3d6da-106">Die Funktionen " [**glgetmaterialfv**](glgetmaterialfv.md) " und " **glgetmaterialiv** " geben Materialparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6da-106">The [**glGetMaterialfv**](glgetmaterialfv.md) and **glGetMaterialiv** functions return material parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6da-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d6da-107">Syntax</span></span>


```C++
void WINAPI glGetMaterialiv(
   GLenum face,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="3d6da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d6da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6da-109">*mit*</span><span class="sxs-lookup"><span data-stu-id="3d6da-109">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6da-110">Gibt an, welches der beiden Materialien abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="3d6da-110">Specifies which of the two materials is being queried.</span></span> <span data-ttu-id="3d6da-111">GL \_ -Front-oder-GL \_ -Back wird akzeptiert und repräsentiert jeweils die Vorder-bzw. Back Materialien.</span><span class="sxs-lookup"><span data-stu-id="3d6da-111">GL\_FRONT or GL\_BACK are accepted, representing the front and back materials, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="3d6da-112">*pName*</span><span class="sxs-lookup"><span data-stu-id="3d6da-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6da-113">Der zurück zugebende Materialparameter.</span><span class="sxs-lookup"><span data-stu-id="3d6da-113">The material parameter to return.</span></span> <span data-ttu-id="3d6da-114">Die folgenden Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="3d6da-114">The following values are accepted.</span></span>



| <span data-ttu-id="3d6da-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3d6da-115">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="3d6da-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3d6da-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="3d6da-117"><dt>**GL- \_ AMBIENT**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-117"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                    | <span data-ttu-id="3d6da-118">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Umgebungs Reflektion des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="3d6da-118">The *params* parameter returns four integer or floating-point values representing the ambient reflectance of the material.</span></span> <span data-ttu-id="3d6da-119">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d6da-119">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="3d6da-120">Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3d6da-120">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="3d6da-121"><dt>**GL- \_ diffuses**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-121"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                    | <span data-ttu-id="3d6da-122">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die diffuse Reflektion des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="3d6da-122">The *params* parameter returns four integer or floating-point values representing the diffuse reflectance of the material.</span></span> <span data-ttu-id="3d6da-123">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d6da-123">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="3d6da-124">Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3d6da-124">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="3d6da-125"><dt>**GL \_ Glanz**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-125"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                 | <span data-ttu-id="3d6da-126">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Glanz Reflektion des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="3d6da-126">The *params* parameter returns four integer or floating-point values representing the specular reflectance of the material.</span></span> <span data-ttu-id="3d6da-127">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d6da-127">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="3d6da-128">Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3d6da-128">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="3d6da-129"><dt>**GL \_ -Ausgabe**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-129"><dt>**GL\_EMISSION**</dt></span></span> </dl>                 | <span data-ttu-id="3d6da-130">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die ausgegebene helle Intensität des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="3d6da-130">The *params* parameter returns four integer or floating-point values representing the emitted light intensity of the material.</span></span> <span data-ttu-id="3d6da-131">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d6da-131">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="3d6da-132">Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="3d6da-132">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="3d6da-133"><dt>**GL \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-133"><dt>**GL\_SHININESS**</dt></span></span> </dl>              | <span data-ttu-id="3d6da-134">Der Parameter *para* meters gibt eine ganze Zahl oder einen Gleit Komma Wert zurück, der den Glanz Exponenten des Materials darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d6da-134">The *params* parameter returns one integer or floating-point value representing the specular exponent of the material.</span></span> <span data-ttu-id="3d6da-135">Ganzzahlige Werte werden, wenn angefordert, berechnet, indem der interne Gleit Komma Wert auf den nächsten ganzzahligen Wert gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="3d6da-135">Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="3d6da-136"><dt>**GL- \_ Farb \_ Indizes**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-136"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl> | <span data-ttu-id="3d6da-137">Der Parameter *para* meters gibt drei ganzzahlige Werte oder Gleit Komma Werte zurück, die die Umgebungs-, diffusen und Glanz Indizes des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="3d6da-137">The *params* parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material.</span></span> <span data-ttu-id="3d6da-138">Verwenden Sie diese Indizes nur für die Farb Index Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="3d6da-138">Use these indexes only for color-index lighting.</span></span> <span data-ttu-id="3d6da-139">(Die anderen Parameter werden nur für die RGBA-Beleuchtung verwendet.) Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf die nächstgelegenen ganzzahligen Werte gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="3d6da-139">(The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                            |



 

</dd> <dt>

<span data-ttu-id="3d6da-140">*params*</span><span class="sxs-lookup"><span data-stu-id="3d6da-140">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6da-141">Gibt die angeforderten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6da-141">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6da-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d6da-142">Return value</span></span>

<span data-ttu-id="3d6da-143">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6da-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d6da-144">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3d6da-144">Error codes</span></span>

<span data-ttu-id="3d6da-145">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3d6da-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3d6da-146">Name</span><span class="sxs-lookup"><span data-stu-id="3d6da-146">Name</span></span>                                                                                                  | <span data-ttu-id="3d6da-147">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3d6da-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d6da-148"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3d6da-149">Das *Ziel* oder die *Abfrage* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="3d6da-149">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="3d6da-150"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3d6da-151">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3d6da-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3d6da-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d6da-152">Remarks</span></span>

<span data-ttu-id="3d6da-153">Die Funktion " **glgetmaterial** " gibt in den *para* Metern den Wert oder die Werte des Parameters " *PName* " der materiellen *Fläche* zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6da-153">The **glGetMaterial** function returns in *params* the value or values of parameter *pname* of material *face*.</span></span>

<span data-ttu-id="3d6da-154">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *para* Metern vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="3d6da-154">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6da-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d6da-155">Requirements</span></span>



| <span data-ttu-id="3d6da-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d6da-156">Requirement</span></span> | <span data-ttu-id="3d6da-157">Wert</span><span class="sxs-lookup"><span data-stu-id="3d6da-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6da-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d6da-158">Minimum supported client</span></span><br/> | <span data-ttu-id="3d6da-159">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d6da-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3d6da-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d6da-160">Minimum supported server</span></span><br/> | <span data-ttu-id="3d6da-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d6da-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d6da-162">Header</span><span class="sxs-lookup"><span data-stu-id="3d6da-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d6da-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3d6da-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d6da-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d6da-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d6da-166">DLL</span><span class="sxs-lookup"><span data-stu-id="3d6da-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d6da-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d6da-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d6da-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d6da-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6da-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3d6da-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3d6da-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3d6da-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3d6da-171">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="3d6da-171">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





