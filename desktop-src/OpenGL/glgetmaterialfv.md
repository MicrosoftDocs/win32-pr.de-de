---
title: glgetmaterialfv-Funktion (GL. h)
description: Die Funktionen "glgetmaterialfv" und "glgetmaterialiv" geben Materialparameter zurück. | glgetmaterialfv-Funktion (GL. h)
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
keywords:
- glgetmaterialfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce33ee1f88d492f67cf3ebb93c575f8f36d1ffa0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352529"
---
# <a name="glgetmaterialfv-function"></a><span data-ttu-id="0b924-105">glgetmaterialfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="0b924-105">glGetMaterialfv function</span></span>

<span data-ttu-id="0b924-106">Die Funktionen " **glgetmaterialfv** " und " [**glgetmaterialiv**](glgetmaterialiv.md) " geben Materialparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="0b924-106">The **glGetMaterialfv** and [**glGetMaterialiv**](glgetmaterialiv.md) functions return material parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b924-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b924-107">Syntax</span></span>


```C++
void WINAPI glGetMaterialfv(
   GLenum  face,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="0b924-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b924-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b924-109">*mit*</span><span class="sxs-lookup"><span data-stu-id="0b924-109">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="0b924-110">Gibt an, welches der beiden Materialien abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="0b924-110">Specifies which of the two materials is being queried.</span></span> <span data-ttu-id="0b924-111">GL \_ -Front-oder-GL \_ -Back wird akzeptiert und repräsentiert jeweils die Vorder-bzw. Back Materialien.</span><span class="sxs-lookup"><span data-stu-id="0b924-111">GL\_FRONT or GL\_BACK are accepted, representing the front and back materials, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="0b924-112">*pName*</span><span class="sxs-lookup"><span data-stu-id="0b924-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="0b924-113">Der zurück zugebende Materialparameter.</span><span class="sxs-lookup"><span data-stu-id="0b924-113">The material parameter to return.</span></span> <span data-ttu-id="0b924-114">Die folgenden Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="0b924-114">The following values are accepted.</span></span>



| <span data-ttu-id="0b924-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0b924-115">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="0b924-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0b924-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="0b924-117"><dt>**GL- \_ AMBIENT**</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-117"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                    | <span data-ttu-id="0b924-118">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Umgebungs Reflektion des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b924-118">The *params* parameter returns four integer or floating-point values representing the ambient reflectance of the material.</span></span> <span data-ttu-id="0b924-119">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0b924-119">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="0b924-120">Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0b924-120">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="0b924-121"><dt>**GL- \_ diffuses**</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-121"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                    | <span data-ttu-id="0b924-122">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die diffuse Reflektion des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b924-122">The *params* parameter returns four integer or floating-point values representing the diffuse reflectance of the material.</span></span> <span data-ttu-id="0b924-123">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0b924-123">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="0b924-124">Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0b924-124">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="0b924-125"><dt>**GL \_ Glanz**</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-125"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                 | <span data-ttu-id="0b924-126">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die Glanz Reflektion des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b924-126">The *params* parameter returns four integer or floating-point values representing the specular reflectance of the material.</span></span> <span data-ttu-id="0b924-127">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0b924-127">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="0b924-128">Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0b924-128">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="0b924-129"><dt>**GL \_ -Ausgabe**</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-129"><dt>**GL\_EMISSION**</dt></span></span> </dl>                 | <span data-ttu-id="0b924-130">Der Parameter *para* meters gibt vier ganzzahlige Werte oder Gleit Komma Werte zurück, die die ausgegebene helle Intensität des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b924-130">The *params* parameter returns four integer or floating-point values representing the emitted light intensity of the material.</span></span> <span data-ttu-id="0b924-131">Ganzzahlige Werte werden, wenn angefordert, linear von der internen Gleit Komma Darstellung zugeordnet, sodass 1,0 dem positivsten darstellbaren ganzzahligen Wert zugeordnet wird und-1,0 dem negativsten darstellbaren ganzzahligen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0b924-131">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="0b924-132">Liegt der interne Wert außerhalb des Bereichs \[ -1, \] ist der entsprechende ganzzahlige Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0b924-132">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="0b924-133"><dt>**GL \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-133"><dt>**GL\_SHININESS**</dt></span></span> </dl>              | <span data-ttu-id="0b924-134">Der Parameter *para* meters gibt eine ganze Zahl oder einen Gleit Komma Wert zurück, der den Glanz Exponenten des Materials darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b924-134">The *params* parameter returns one integer or floating-point value representing the specular exponent of the material.</span></span> <span data-ttu-id="0b924-135">Ganzzahlige Werte werden, wenn angefordert, berechnet, indem der interne Gleit Komma Wert auf den nächsten ganzzahligen Wert gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="0b924-135">Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="0b924-136"><dt>**GL- \_ Farb \_ Indizes**</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-136"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl> | <span data-ttu-id="0b924-137">Der Parameter *para* meters gibt drei ganzzahlige Werte oder Gleit Komma Werte zurück, die die Umgebungs-, diffusen und Glanz Indizes des Materials darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b924-137">The *params* parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material.</span></span> <span data-ttu-id="0b924-138">Verwenden Sie diese Indizes nur für die Farb Index Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="0b924-138">Use these indexes only for color-index lighting.</span></span> <span data-ttu-id="0b924-139">(Die anderen Parameter werden nur für die RGBA-Beleuchtung verwendet.) Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf die nächstgelegenen ganzzahligen Werte gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="0b924-139">(The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                            |



 

</dd> <dt>

<span data-ttu-id="0b924-140">*params*</span><span class="sxs-lookup"><span data-stu-id="0b924-140">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="0b924-141">Gibt die angeforderten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="0b924-141">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b924-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b924-142">Return value</span></span>

<span data-ttu-id="0b924-143">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0b924-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b924-144">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0b924-144">Error codes</span></span>

<span data-ttu-id="0b924-145">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0b924-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0b924-146">Name</span><span class="sxs-lookup"><span data-stu-id="0b924-146">Name</span></span>                                                                                                  | <span data-ttu-id="0b924-147">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0b924-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b924-148"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0b924-149">Das *Ziel* oder die *Abfrage* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="0b924-149">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="0b924-150"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0b924-151">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0b924-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0b924-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b924-152">Remarks</span></span>

<span data-ttu-id="0b924-153">Die Funktion " **glgetmaterial** " gibt in den *para* Metern den Wert oder die Werte des Parameters " *PName* " der materiellen *Fläche* zurück.</span><span class="sxs-lookup"><span data-stu-id="0b924-153">The **glGetMaterial** function returns in *params* the value or values of parameter *pname* of material *face*.</span></span>

<span data-ttu-id="0b924-154">Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *para* Metern vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="0b924-154">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b924-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b924-155">Requirements</span></span>



| <span data-ttu-id="0b924-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b924-156">Requirement</span></span> | <span data-ttu-id="0b924-157">Wert</span><span class="sxs-lookup"><span data-stu-id="0b924-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b924-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b924-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0b924-159">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b924-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0b924-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b924-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0b924-161">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b924-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0b924-162">Header</span><span class="sxs-lookup"><span data-stu-id="0b924-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b924-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0b924-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b924-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b924-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0b924-166">DLL</span><span class="sxs-lookup"><span data-stu-id="0b924-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b924-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b924-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b924-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b924-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b924-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0b924-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0b924-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0b924-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0b924-171">**glmaterial**</span><span class="sxs-lookup"><span data-stu-id="0b924-171">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





