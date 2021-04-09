---
title: gltexenvf-Funktion (GL. h)
description: Die gltexenvf-Funktion legt einen Texture-Umgebungsparameter fest.
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- gltexenvf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1566378b6dcd2f91a2e2cd445f0ec39c0f6f6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741128"
---
# <a name="gltexenvf-function"></a><span data-ttu-id="71580-104">gltexenvf-Funktion</span><span class="sxs-lookup"><span data-stu-id="71580-104">glTexEnvf function</span></span>

<span data-ttu-id="71580-105">Die **gltexenvf** -Funktion legt einen Texture-Umgebungsparameter fest.</span><span class="sxs-lookup"><span data-stu-id="71580-105">The **glTexEnvf** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="71580-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="71580-106">Syntax</span></span>


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="71580-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="71580-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71580-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="71580-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="71580-109">Eine Textur Umgebung.</span><span class="sxs-lookup"><span data-stu-id="71580-109">A texture environment.</span></span> <span data-ttu-id="71580-110">Muss "GL \_ Texture" sein \_ .</span><span class="sxs-lookup"><span data-stu-id="71580-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="71580-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="71580-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="71580-112">Der symbolische Name eines einwertigen Textur Umgebungs Parameters.</span><span class="sxs-lookup"><span data-stu-id="71580-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="71580-113">Muss der GL- \_ Textur \_ env-Modus sein \_ .</span><span class="sxs-lookup"><span data-stu-id="71580-113">Must be GL\_TEXTURE\_ENV\_MODE.</span></span>

</dd> <dt>

<span data-ttu-id="71580-114">*param*</span><span class="sxs-lookup"><span data-stu-id="71580-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="71580-115">Eine einzelne symbolische Konstante, eine von GL \_ Modulate, GL \_ , GL, GL \_ Blend oder GL \_ Replace.</span><span class="sxs-lookup"><span data-stu-id="71580-115">A single symbolic constant, one of GL\_MODULATE, GL\_DECAL, GL\_BLEND, or GL\_REPLACE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71580-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71580-116">Return value</span></span>

<span data-ttu-id="71580-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71580-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71580-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="71580-118">Error codes</span></span>

<span data-ttu-id="71580-119">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71580-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71580-120">Name</span><span class="sxs-lookup"><span data-stu-id="71580-120">Name</span></span>                                                                                                  | <span data-ttu-id="71580-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71580-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71580-122"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71580-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="71580-123">*target* oder *PName* war keiner der akzeptierten definierten Werte, oder wenn Parameter einen definierten Konstanten Wert *aufweisen sollten (* basierend auf dem Wert von *PName*), und nicht.</span><span class="sxs-lookup"><span data-stu-id="71580-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="71580-124"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="71580-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71580-125">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="71580-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="71580-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71580-126">Remarks</span></span>

<span data-ttu-id="71580-127">Eine Textur Umgebung gibt an, wie Textur Werte interpretiert werden, wenn ein Fragment strukturiert ist.</span><span class="sxs-lookup"><span data-stu-id="71580-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="71580-128">Der *Ziel* Parameter muss "GL \_ Texture" sein \_ .</span><span class="sxs-lookup"><span data-stu-id="71580-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="71580-129">Der *PName* -Parameter ist der GL- \_ Textur \_ env- \_ Modus.</span><span class="sxs-lookup"><span data-stu-id="71580-129">The *pname* parameter is GL\_TEXTURE\_ENV\_MODE.</span></span> <span data-ttu-id="71580-130">Drei Textur Funktionen sind definiert: GL \_ Modulate, GL \_ Decal und GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="71580-130">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="71580-131">Eine Textur Funktion wird für das Fragment verwendet, das mit dem Textur bildrwert, der für das Fragment gilt (siehe [**gltexparameter**](gltexparameter-functions.md)), strukturiert werden soll, und erzeugt eine RGBA-Farbe für dieses Fragment.</span><span class="sxs-lookup"><span data-stu-id="71580-131">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="71580-132">In der folgenden Tabelle wird gezeigt, wie die RGBA-Farbe für jede der drei Textur Funktionen erstellt wird, die ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="71580-132">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="71580-133">*C* ist ein dreifaches von Farbwerten (RGB), und *ein* ist der zugeordnete Alphawert.</span><span class="sxs-lookup"><span data-stu-id="71580-133">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="71580-134">Aus einem Textur Bild extrahierte RGBA-Werte liegen im Bereich von \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="71580-134">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="71580-135">Der Index " *f* " bezieht sich auf das eingehende Fragment, *das für das* Textur Bild, den Index " *c* " für die Textur Umgebungs Farbe und "Index *v* " einen Wert, der von der Textur Funktion erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="71580-135">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="71580-136">Ein Textur Bild kann bis zu vier Komponenten pro Textur Element aufweisen (siehe [**glTexImage1D**](glteximage1d.md) und [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="71580-136">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="71580-137">In einem einkomponentenbild gibt lt diese einzelne Komponente an.</span><span class="sxs-lookup"><span data-stu-id="71580-137">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="71580-138">Ein Image mit zwei Komponenten verwendet *L?*</span><span class="sxs-lookup"><span data-stu-id="71580-138">A two-component image uses *L?*</span></span>  <span data-ttu-id="71580-139">und *A?*</span><span class="sxs-lookup"><span data-stu-id="71580-139">and *A?*</span></span> <span data-ttu-id="71580-140">.</span><span class="sxs-lookup"><span data-stu-id="71580-140">.</span></span> <span data-ttu-id="71580-141">Ein Image mit drei Komponenten hat nur einen Farbwert, *C?*</span><span class="sxs-lookup"><span data-stu-id="71580-141">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="71580-142">.</span><span class="sxs-lookup"><span data-stu-id="71580-142">.</span></span> <span data-ttu-id="71580-143">Ein Image mit vier Komponenten hat beide den Farbwert *C?*</span><span class="sxs-lookup"><span data-stu-id="71580-143">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="71580-144">und ein Alpha Wert *A?*</span><span class="sxs-lookup"><span data-stu-id="71580-144">and an alpha value *A?*</span></span> <span data-ttu-id="71580-145">.</span><span class="sxs-lookup"><span data-stu-id="71580-145">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="71580-146">Anzahl von Komponenten</span><span class="sxs-lookup"><span data-stu-id="71580-146">Number of components</span></span></th>
<th><span data-ttu-id="71580-147">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="71580-147">GL_MODULATE</span></span></th>
<th><span data-ttu-id="71580-148">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="71580-148">GL_DECAL</span></span></th>
<th><span data-ttu-id="71580-149">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="71580-149">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="71580-150">1 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="71580-150">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="71580-151"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="71580-151"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="71580-152"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="71580-152"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="71580-153">nicht definiertes $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="71580-153">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="71580-154"><em>C</em> <em><sub>v</sub></em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="71580-154"><em>C</em> <em><sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="71580-155"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="71580-155"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="71580-156"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="71580-156"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71580-157"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="71580-157"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="71580-158"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="71580-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="71580-159">2 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="71580-159">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="71580-160"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="71580-160"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="71580-161"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="71580-161"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="71580-162">nicht definiertes $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="71580-162">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="71580-163"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="71580-163"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="71580-164"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="71580-164"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="71580-165"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="71580-165"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71580-166"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="71580-166"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="71580-167"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="71580-167"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="71580-168">3 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="71580-168">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="71580-169"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="71580-169"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="71580-170"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="71580-170"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="71580-171"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="71580-171"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="71580-172">nicht definiertes $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="71580-172">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="71580-173"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="71580-173"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="71580-174"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="71580-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="71580-175">4 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="71580-175">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="71580-176"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="71580-176"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="71580-177"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="71580-177"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="71580-178"><em>C<sub>v</sub> </em> = (1- <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="71580-178"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="71580-179"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="71580-179"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="71580-180"><em>Scher?</em></span><span class="sxs-lookup"><span data-stu-id="71580-180"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="71580-181">nicht definiertes $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="71580-181">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="71580-182"><em>A<sub>v</sub> </em>  =  <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="71580-182"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="71580-183"><em>A<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="71580-183"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="71580-184"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="71580-184"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="71580-185">Der GL- \_ Textur \_ env- \_ Modus ist standardmäßig GL \_ modulate.</span><span class="sxs-lookup"><span data-stu-id="71580-185">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE.</span></span>

<span data-ttu-id="71580-186">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexenvf** ab:</span><span class="sxs-lookup"><span data-stu-id="71580-186">The following function retrieves information related to **glTexEnvf**:</span></span>

[<span data-ttu-id="71580-187">**gltexgetenvfv**</span><span class="sxs-lookup"><span data-stu-id="71580-187">**glTexGetEnvfv**</span></span>](glgettexenvfv.md)

## <a name="requirements"></a><span data-ttu-id="71580-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71580-188">Requirements</span></span>



| <span data-ttu-id="71580-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71580-189">Requirement</span></span> | <span data-ttu-id="71580-190">Wert</span><span class="sxs-lookup"><span data-stu-id="71580-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71580-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71580-191">Minimum supported client</span></span><br/> | <span data-ttu-id="71580-192">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71580-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71580-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71580-193">Minimum supported server</span></span><br/> | <span data-ttu-id="71580-194">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71580-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71580-195">Header</span><span class="sxs-lookup"><span data-stu-id="71580-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="71580-196"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71580-196"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71580-197">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71580-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="71580-198"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71580-198"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71580-199">DLL</span><span class="sxs-lookup"><span data-stu-id="71580-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71580-200"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71580-200"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71580-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71580-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71580-202">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71580-202">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71580-203">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71580-203">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71580-204">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="71580-204">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="71580-205">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="71580-205">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="71580-206">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="71580-206">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





