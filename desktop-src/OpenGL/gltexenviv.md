---
title: gltexenviv-Funktion (GL. h)
description: Die gltexenviv-Funktion legt einen Texture-Umgebungsparameter fest.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- gltexenviv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ec232f559e8d4af10369ebe98dd0aea71e36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859302"
---
# <a name="gltexenviv-function"></a><span data-ttu-id="51164-104">gltexenviv-Funktion</span><span class="sxs-lookup"><span data-stu-id="51164-104">glTexEnviv function</span></span>

<span data-ttu-id="51164-105">Die **gltexenviv** -Funktion legt einen Texture-Umgebungsparameter fest.</span><span class="sxs-lookup"><span data-stu-id="51164-105">The **glTexEnviv** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="51164-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="51164-106">Syntax</span></span>


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="51164-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="51164-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51164-108">*Ziel*</span><span class="sxs-lookup"><span data-stu-id="51164-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="51164-109">Eine Textur Umgebung.</span><span class="sxs-lookup"><span data-stu-id="51164-109">A texture environment.</span></span> <span data-ttu-id="51164-110">Muss "GL \_ Texture" sein \_ .</span><span class="sxs-lookup"><span data-stu-id="51164-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="51164-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="51164-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="51164-112">Der symbolische Name eines einwertigen Textur Umgebungs Parameters.</span><span class="sxs-lookup"><span data-stu-id="51164-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="51164-113">Akzeptierte Werte sind der \_ GL \_ -Textur env \_ -Modus und die GL- \_ Textur \_ env- \_ Farbe.</span><span class="sxs-lookup"><span data-stu-id="51164-113">Accepted values are GL\_TEXTURE\_ENV\_MODE and GL\_TEXTURE\_ENV\_COLOR.</span></span>

</dd> <dt>

<span data-ttu-id="51164-114">*params*</span><span class="sxs-lookup"><span data-stu-id="51164-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="51164-115">Ein Zeiger auf ein Array von Parametern: entweder eine einzelne symbolische Konstante oder eine RGBA-Farbe.</span><span class="sxs-lookup"><span data-stu-id="51164-115">A pointer to an array of parameters: either a single symbolic constant or an RGBA color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51164-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51164-116">Return value</span></span>

<span data-ttu-id="51164-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="51164-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="51164-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="51164-118">Error codes</span></span>

<span data-ttu-id="51164-119">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="51164-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="51164-120">Name</span><span class="sxs-lookup"><span data-stu-id="51164-120">Name</span></span>                                                                                                  | <span data-ttu-id="51164-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="51164-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51164-122"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="51164-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="51164-123">*target* oder *PName* war keiner der akzeptierten definierten Werte, oder wenn Parameter einen definierten Konstanten Wert *aufweisen sollten (* basierend auf dem Wert von *PName*), und nicht.</span><span class="sxs-lookup"><span data-stu-id="51164-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="51164-124"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="51164-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="51164-125">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="51164-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="51164-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51164-126">Remarks</span></span>

<span data-ttu-id="51164-127">Eine Textur Umgebung gibt an, wie Textur Werte interpretiert werden, wenn ein Fragment strukturiert ist.</span><span class="sxs-lookup"><span data-stu-id="51164-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="51164-128">Der *Ziel* Parameter muss "GL \_ Texture" sein \_ .</span><span class="sxs-lookup"><span data-stu-id="51164-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="51164-129">Der *PName* -Parameter kann entweder der GL- \_ Textur \_ env- \_ Modus oder die GL- \_ Textur \_ env- \_ Farbe sein.</span><span class="sxs-lookup"><span data-stu-id="51164-129">The *pname* parameter can be either GL\_TEXTURE\_ENV\_MODE or GL\_TEXTURE\_ENV\_COLOR.</span></span>

<span data-ttu-id="51164-130">Wenn *PName* den GL- \_ Textur \_ env- \_ Modus  hat, ist der symbolische Name einer Textur Funktion (oder verweist auf diesen).</span><span class="sxs-lookup"><span data-stu-id="51164-130">If *pname* is GL\_TEXTURE\_ENV\_MODE, then *params* is (or points to) the symbolic name of a texture function.</span></span> <span data-ttu-id="51164-131">Drei Textur Funktionen sind definiert: GL \_ Modulate, GL \_ Decal und GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="51164-131">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="51164-132">Eine Textur Funktion wird für das Fragment verwendet, das mit dem Textur bildrwert, der für das Fragment gilt (siehe [**gltexparameter**](gltexparameter-functions.md)), strukturiert werden soll, und erzeugt eine RGBA-Farbe für dieses Fragment.</span><span class="sxs-lookup"><span data-stu-id="51164-132">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="51164-133">In der folgenden Tabelle wird gezeigt, wie die RGBA-Farbe für jede der drei Textur Funktionen erstellt wird, die ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="51164-133">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="51164-134">*C* ist ein dreifaches von Farbwerten (RGB), und *ein* ist der zugeordnete Alphawert.</span><span class="sxs-lookup"><span data-stu-id="51164-134">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="51164-135">Aus einem Textur Bild extrahierte RGBA-Werte liegen im Bereich von \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="51164-135">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="51164-136">Der Index " *f* " bezieht sich auf das eingehende Fragment, *das für das* Textur Bild, den Index " *c* " für die Textur Umgebungs Farbe und "Index *v* " einen Wert, der von der Textur Funktion erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="51164-136">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="51164-137">Ein Textur Bild kann bis zu vier Komponenten pro Textur Element aufweisen (siehe [**glTexImage1D**](glteximage1d.md) und [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="51164-137">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="51164-138">In einem einkomponentenbild gibt lt diese einzelne Komponente an.</span><span class="sxs-lookup"><span data-stu-id="51164-138">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="51164-139">Ein Image mit zwei Komponenten verwendet *L?*</span><span class="sxs-lookup"><span data-stu-id="51164-139">A two-component image uses *L?*</span></span>  <span data-ttu-id="51164-140">und *A?*</span><span class="sxs-lookup"><span data-stu-id="51164-140">and *A?*</span></span> <span data-ttu-id="51164-141">.</span><span class="sxs-lookup"><span data-stu-id="51164-141">.</span></span> <span data-ttu-id="51164-142">Ein Image mit drei Komponenten hat nur einen Farbwert, *C?*</span><span class="sxs-lookup"><span data-stu-id="51164-142">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="51164-143">.</span><span class="sxs-lookup"><span data-stu-id="51164-143">.</span></span> <span data-ttu-id="51164-144">Ein Image mit vier Komponenten hat beide den Farbwert *C?*</span><span class="sxs-lookup"><span data-stu-id="51164-144">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="51164-145">und ein Alpha Wert *A?*</span><span class="sxs-lookup"><span data-stu-id="51164-145">and an alpha value *A?*</span></span> <span data-ttu-id="51164-146">.</span><span class="sxs-lookup"><span data-stu-id="51164-146">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="51164-147">Anzahl von Komponenten</span><span class="sxs-lookup"><span data-stu-id="51164-147">Number of components</span></span></th>
<th><span data-ttu-id="51164-148">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="51164-148">GL_MODULATE</span></span></th>
<th><span data-ttu-id="51164-149">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="51164-149">GL_DECAL</span></span></th>
<th><span data-ttu-id="51164-150">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="51164-150">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="51164-151">1 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="51164-151">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="51164-152"><em>C<sub>v</sub> </em>   =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="51164-152"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="51164-153"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="51164-153"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="51164-154">nicht definiertes $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="51164-154">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="51164-155"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="51164-155"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="51164-156"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="51164-156"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="51164-157"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="51164-157"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51164-158"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="51164-158"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="51164-159"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="51164-159"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="51164-160">2 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="51164-160">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="51164-161"><em>C<sub>v</sub> </em>   =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="51164-161"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="51164-162"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="51164-162"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="51164-163">nicht definiertes $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="51164-163">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="51164-164"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="51164-164"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="51164-165"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="51164-165"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="51164-166"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="51164-166"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51164-167"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="51164-167"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="51164-168"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="51164-168"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="51164-169">3 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="51164-169">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="51164-170"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="51164-170"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="51164-171"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="51164-171"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="51164-172"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="51164-172"><em>C<sub>v</sub></em>  = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="51164-173">nicht definiertes $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="51164-173">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="51164-174"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="51164-174"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="51164-175"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="51164-175"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="51164-176">4 $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="51164-176">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="51164-177"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="51164-177"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="51164-178"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="51164-178"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="51164-179"><em>C<sub>v</sub> </em> = (1- <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="51164-179"><em>C<sub>v</sub></em>  = (1 - <em>A?</em></span></span> <span data-ttu-id="51164-180"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="51164-180"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="51164-181"><em>Scher?</em></span><span class="sxs-lookup"><span data-stu-id="51164-181"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="51164-182">nicht definiertes $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="51164-182">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="51164-183"><em>A<sub>v</sub> </em>   =  <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="51164-183"><em>A<sub>v</sub></em>  = <em>A?</em></span></span> <span data-ttu-id="51164-184"><em>A<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="51164-184"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="51164-185"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="51164-185"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="51164-186">Wenn pName eine GL- \_ Textur \_ env-Farbe ist \_ , ist *params* ein Zeiger auf ein Array, das eine aus vier Werten bestehenden RGBA-Farbe enthält.</span><span class="sxs-lookup"><span data-stu-id="51164-186">If pname is GL\_TEXTURE\_ENV\_COLOR, *params* is a pointer to an array that holds an RGBA color consisting of four values.</span></span> <span data-ttu-id="51164-187">Ganzzahlige Farbkomponenten werden linear interpretiert, sodass die positive ganze Zahl 1,0 und die negativste Ganzzahl "-1,0" zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="51164-187">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to -1.0.</span></span> <span data-ttu-id="51164-188">Die Werte werden an den Bereich \[ 0, 1 gebunden, \] Wenn Sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51164-188">The values are clamped to the range \[0, 1\] when they are specified.</span></span> <span data-ttu-id="51164-189">*C <sub>c</sub>* übernimmt diese vier Werte.</span><span class="sxs-lookup"><span data-stu-id="51164-189">*C<sub>c</sub>* takes these four values.</span></span>

<span data-ttu-id="51164-190">Der \_ GL \_ -Textur env \_ -Modus wird standardmäßig auf GL \_ modulate und \_ die Standardfarbe der GL-Textur \_ env \_ auf (0, 0, 0, 0) eingestellt.</span><span class="sxs-lookup"><span data-stu-id="51164-190">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE and GL\_TEXTURE\_ENV\_COLOR defaults to (0, 0, 0, 0).</span></span>

<span data-ttu-id="51164-191">Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexenviv** ab:</span><span class="sxs-lookup"><span data-stu-id="51164-191">The following function retrieves information related to **glTexEnviv**:</span></span>

[<span data-ttu-id="51164-192">**gltexgetenviv**</span><span class="sxs-lookup"><span data-stu-id="51164-192">**glTexGetEnviv**</span></span>](glgettexenviv.md)

## <a name="requirements"></a><span data-ttu-id="51164-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51164-193">Requirements</span></span>



| <span data-ttu-id="51164-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51164-194">Requirement</span></span> | <span data-ttu-id="51164-195">Wert</span><span class="sxs-lookup"><span data-stu-id="51164-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51164-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51164-196">Minimum supported client</span></span><br/> | <span data-ttu-id="51164-197">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51164-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="51164-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51164-198">Minimum supported server</span></span><br/> | <span data-ttu-id="51164-199">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51164-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51164-200">Header</span><span class="sxs-lookup"><span data-stu-id="51164-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="51164-201"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="51164-201"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="51164-202">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="51164-202">Library</span></span><br/>                  | <dl> <span data-ttu-id="51164-203"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51164-203"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="51164-204">DLL</span><span class="sxs-lookup"><span data-stu-id="51164-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51164-205"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51164-205"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51164-206">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51164-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51164-207">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="51164-207">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="51164-208">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="51164-208">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="51164-209">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="51164-209">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="51164-210">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="51164-210">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="51164-211">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="51164-211">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





