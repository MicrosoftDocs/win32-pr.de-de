---
title: glmaterialfv-Funktion (GL. h)
description: Die glmaterialfv-Funktion gibt Materialparameter für das Beleuchtungsmodell an.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- glmaterialfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44b200abe0588a657f770902a9a897329e1942a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391504"
---
# <a name="glmaterialfv-function"></a><span data-ttu-id="8911a-104">glmaterialfv-Funktion</span><span class="sxs-lookup"><span data-stu-id="8911a-104">glMaterialfv function</span></span>

<span data-ttu-id="8911a-105">Die **glmaterialfv** -Funktion gibt Materialparameter für das Beleuchtungsmodell an.</span><span class="sxs-lookup"><span data-stu-id="8911a-105">The **glMaterialfv** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="8911a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8911a-106">Syntax</span></span>


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="8911a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8911a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8911a-108">*mit*</span><span class="sxs-lookup"><span data-stu-id="8911a-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="8911a-109">Die Gesichter oder Gesichter, die aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8911a-109">The face or faces that are being updated.</span></span> <span data-ttu-id="8911a-110">Muss eines der folgenden sein: GL \_ Front, GL \_ Back, GL \_ Front und GL \_ Back.</span><span class="sxs-lookup"><span data-stu-id="8911a-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="8911a-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="8911a-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="8911a-112">Der Materialparameter der Gesichts-oder Gesichter, die aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8911a-112">The material parameter of the face or faces being updated.</span></span> <span data-ttu-id="8911a-113">Die Parameter, die mit **glmaterialfv** angegeben werden können, und ihre Interpretationen durch die Beleuchtungs Gleichung lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="8911a-113">The parameters that can be specified using **glMaterialfv**, and their interpretations by the lighting equation, are as follows.</span></span>



| <span data-ttu-id="8911a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8911a-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="8911a-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8911a-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="8911a-116"><dt>**GL- \_ AMBIENT**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-116"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                                       | <span data-ttu-id="8911a-117">Der Parameter Parameters enthält vier Gleit Komma Werte, die die Ambiente-RGBA-Reflektion des Materials angeben.</span><span class="sxs-lookup"><span data-stu-id="8911a-117">The params parameter contains four floating-point values that specify the ambient RGBA reflectance of the material.</span></span> <span data-ttu-id="8911a-118">Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0.</span><span class="sxs-lookup"><span data-stu-id="8911a-118">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="8911a-119">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8911a-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="8911a-120">Keine ganzzahligen oder Gleit Komma Werte werden geklammert.</span><span class="sxs-lookup"><span data-stu-id="8911a-120">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="8911a-121">Die standardmäßige Umgebungs Reflektion für die Vorder-und Hintergrundmaterialien ist (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="8911a-121">The default ambient reflectance for both front-facing and back-facing materials is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="8911a-122"><dt>**GL- \_ diffuses**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-122"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="8911a-123">Der Parameter Parameters enthält vier Gleit Komma Werte, die die diffuse RGBA-Reflektion des Materials angeben.</span><span class="sxs-lookup"><span data-stu-id="8911a-123">The params parameter contains four floating-point values that specify the diffuse RGBA reflectance of the material.</span></span> <span data-ttu-id="8911a-124">Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0.</span><span class="sxs-lookup"><span data-stu-id="8911a-124">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="8911a-125">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8911a-125">Floating-point values are mapped directly.</span></span> <span data-ttu-id="8911a-126">Keine ganzzahligen oder Gleit Komma Werte werden geklammert.</span><span class="sxs-lookup"><span data-stu-id="8911a-126">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="8911a-127">Die standardmäßige diffuse Reflektion für die Vorder-und Hintergrundmaterialien ist (0,8, 0,8, 0,8, 1,0).</span><span class="sxs-lookup"><span data-stu-id="8911a-127">The default diffuse reflectance for both front-facing and back-facing materials is (0.8, 0.8, 0.8, 1.0).</span></span> <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="8911a-128"><dt>**GL \_ Glanz**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-128"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                                    | <span data-ttu-id="8911a-129">Der Parameter Parameters enthält vier Gleit Komma Werte, die die Glanz Bare RGBA-Reflektion des Materials angeben.</span><span class="sxs-lookup"><span data-stu-id="8911a-129">The params parameter contains four floating-point values that specify the specular RGBA reflectance of the material.</span></span> <span data-ttu-id="8911a-130">Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0.</span><span class="sxs-lookup"><span data-stu-id="8911a-130">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="8911a-131">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8911a-131">Floating-point values are mapped directly.</span></span> <span data-ttu-id="8911a-132">Keine ganzzahligen oder Gleit Komma Werte werden geklammert.</span><span class="sxs-lookup"><span data-stu-id="8911a-132">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="8911a-133">Die standardmäßige Glanz Reflektion für die Vorder-und Hintergrundmaterialien lautet (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="8911a-133">The default specular reflectance for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="8911a-134"><dt>**GL \_ -Ausgabe**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-134"><dt>**GL\_EMISSION**</dt></span></span> </dl>                                    | <span data-ttu-id="8911a-135">Der Parameter Parameters enthält vier Gleit Komma Werte, die angeben, dass RGBA die helle Intensität des Materials ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8911a-135">The params parameter contains four floating-point values that specify the RGBA emitted light intensity of the material.</span></span> <span data-ttu-id="8911a-136">Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0.</span><span class="sxs-lookup"><span data-stu-id="8911a-136">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="8911a-137">Gleit Komma Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8911a-137">Floating-point values are mapped directly.</span></span> <span data-ttu-id="8911a-138">Keine ganzzahligen oder Gleit Komma Werte werden geklammert.</span><span class="sxs-lookup"><span data-stu-id="8911a-138">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="8911a-139">Die standardmäßige Ausgabe Intensität für die Vorder-und Hintergrundmaterialien ist (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="8911a-139">The default emission intensity for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="8911a-140"><dt>**GL \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-140"><dt>**GL\_SHININESS**</dt></span></span> </dl>                                 | <span data-ttu-id="8911a-141">Der Parameter *param* ist ein einzelner ganzzahliger Wert, der den glänzenden RGBA-Exponent des Materials angibt.</span><span class="sxs-lookup"><span data-stu-id="8911a-141">The *param* parameter is a single integer value that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="8911a-142">Ganzzahlige Werte werden direkt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8911a-142">Integer values are mapped directly.</span></span> <span data-ttu-id="8911a-143">Nur Werte im Bereich von \[ 0, 128 \] werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="8911a-143">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="8911a-144">Der standardmäßige Glanz Exponent für die Vorder-und Hintergrundmaterialien ist 0.</span><span class="sxs-lookup"><span data-stu-id="8911a-144">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <span data-ttu-id="8911a-145"><dt>**GL \_ AMBIENT \_ und \_ diffuse**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-145"><dt>**GL\_AMBIENT\_AND\_DIFFUSE**</dt></span></span> </dl> | <span data-ttu-id="8911a-146">Äquivalent zum doppelten Aufrufen von [**glmaterial**](glmaterial-functions.md) mit denselben Parameterwerten, einmal mit GL \_ AMBIENT und Once mit GL \_ diffus.</span><span class="sxs-lookup"><span data-stu-id="8911a-146">Equivalent to calling [**glMaterial**](glmaterial-functions.md) twice with the same parameter values, once with GL\_AMBIENT and once with GL\_DIFFUSE.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="8911a-147"><dt>**GL- \_ Farb \_ Indizes**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-147"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl>                    | <span data-ttu-id="8911a-148">Der Parameter Parameters enthält drei Gleit Komma Werte, die die Farbindizes für Ambient, diffuse und Glanz Beleuchtung angeben.</span><span class="sxs-lookup"><span data-stu-id="8911a-148">The params parameter contains three floating-point values specifying the color indexes for ambient, diffuse, and specular lighting.</span></span> <span data-ttu-id="8911a-149">Diese drei Werte und GL \_ -Glanz sind die einzigen materiellen Werte, die von der Farb Index Modus-Beleuchtungs Gleichung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8911a-149">These three values, and GL\_SHININESS, are the only material values used by the color-index mode lighting equation.</span></span> <span data-ttu-id="8911a-150">Eine Erläuterung der Farb Index Beleuchtung finden Sie unter [**gllightmodel**](gllightmodel-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="8911a-150">Refer to [**glLightModel**](gllightmodel-functions.md) for a discussion of color-index lighting.</span></span><br/>                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="8911a-151">*params*</span><span class="sxs-lookup"><span data-stu-id="8911a-151">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="8911a-152">Der Wert, auf den der Parameter GL- \_ Glanz festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8911a-152">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8911a-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8911a-153">Return value</span></span>

<span data-ttu-id="8911a-154">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8911a-154">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8911a-155">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8911a-155">Error codes</span></span>

<span data-ttu-id="8911a-156">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8911a-156">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8911a-157">Name</span><span class="sxs-lookup"><span data-stu-id="8911a-157">Name</span></span>                                                                                              | <span data-ttu-id="8911a-158">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8911a-158">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8911a-159"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-159"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="8911a-160">Entweder *Face* oder *PName* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="8911a-160">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="8911a-161"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-161"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="8911a-162">Ein Glanz Exponent außerhalb des Bereichs von \[ 0, 128 \] wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="8911a-162">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8911a-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8911a-163">Remarks</span></span>

<span data-ttu-id="8911a-164">Die Funktion " [**glmaterialfv**](glmaterialf.md) " weist Materialparametern Werte zu.</span><span class="sxs-lookup"><span data-stu-id="8911a-164">The [**glMaterialfv**](glmaterialf.md) function assigns values to material parameters.</span></span> <span data-ttu-id="8911a-165">Es gibt zwei übereinstimmende Sätze von Materialparametern.</span><span class="sxs-lookup"><span data-stu-id="8911a-165">There are two matched sets of material parameters.</span></span> <span data-ttu-id="8911a-166">Eine, die *Front-End-* Gruppe, wird zum Schattieren von Punkten, Linien, Bitmaps und allen Polygonen verwendet (wenn die zweiseitige Beleuchtung deaktiviert ist), oder nur mit Front-End-Polygonen (bei aktivierter zweiseitiger Beleuchtung).</span><span class="sxs-lookup"><span data-stu-id="8911a-166">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="8911a-167">Der andere Satz, mit dem *Hintergrund*, wird verwendet, um nur rückwärts gerichtete Polygone zu schattieren, wenn die zweiseitige Beleuchtung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8911a-167">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="8911a-168">Ausführliche Informationen zu einseitigen und zweiseitigen Beleuchtungsberechnungen finden Sie unter " [**gllightmodel**](gllightmodel-functions.md) ".</span><span class="sxs-lookup"><span data-stu-id="8911a-168">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="8911a-169">Die [**glmaterialfv**](glmaterialf.md) -Funktion erfordert drei Argumente.</span><span class="sxs-lookup"><span data-stu-id="8911a-169">The [**glMaterialfv**](glmaterialf.md) function takes three arguments.</span></span> <span data-ttu-id="8911a-170">*Mit* dem ersten, dem Vordergrund, wird angegeben, ob die GL \_ -Front-Materialien, die GL \_ -Back-Materialien oder die \_ Vorder \_ -und \_ Hintergrundmaterialien von GL geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8911a-170">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="8911a-171">Der zweite Wert, *PName*, gibt an, welche von mehreren Parametern in einem oder beiden Sätzen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8911a-171">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="8911a-172">Der dritte Parameter gibt *an, welcher* Wert dem angegebenen Parameter zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8911a-172">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="8911a-173">Material Parameter werden in der Beleuchtungs Gleichung verwendet, die optional auf jeden Scheitelpunkt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8911a-173">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="8911a-174">Die Gleichung wird in " [**gllightmodel**](gllightmodel-functions.md)" erläutert.</span><span class="sxs-lookup"><span data-stu-id="8911a-174">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="8911a-175">Die Materialparameter können jederzeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8911a-175">The material parameters can be updated at any time.</span></span> <span data-ttu-id="8911a-176">Insbesondere kann [**glmaterialfv**](glmaterialf.md) zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8911a-176">In particular, [**glMaterialfv**](glmaterialf.md) can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="8911a-177">Wenn nur ein einzelner Materialparameter pro Scheitelpunkt geändert werden soll, wird [**glcolormaterial**](glcolormaterial.md) gegenüber **glmaterialfv** bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="8911a-177">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialfv**.</span></span>

<span data-ttu-id="8911a-178">Die folgende Funktion Ruft Informationen im Zusammenhang mit [**glmaterialfv**](glmaterialf.md)ab:</span><span class="sxs-lookup"><span data-stu-id="8911a-178">The following function retrieves information related to [**glMaterialfv**](glmaterialf.md):</span></span>

[<span data-ttu-id="8911a-179">**glgetmaterial**</span><span class="sxs-lookup"><span data-stu-id="8911a-179">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="8911a-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8911a-180">Requirements</span></span>



| <span data-ttu-id="8911a-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8911a-181">Requirement</span></span> | <span data-ttu-id="8911a-182">Wert</span><span class="sxs-lookup"><span data-stu-id="8911a-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8911a-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8911a-183">Minimum supported client</span></span><br/> | <span data-ttu-id="8911a-184">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8911a-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8911a-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8911a-185">Minimum supported server</span></span><br/> | <span data-ttu-id="8911a-186">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8911a-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8911a-187">Header</span><span class="sxs-lookup"><span data-stu-id="8911a-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="8911a-188"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-188"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8911a-189">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8911a-189">Library</span></span><br/>                  | <dl> <span data-ttu-id="8911a-190"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-190"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8911a-191">DLL</span><span class="sxs-lookup"><span data-stu-id="8911a-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8911a-192"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8911a-192"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8911a-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8911a-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8911a-194">**glcolormaterial**</span><span class="sxs-lookup"><span data-stu-id="8911a-194">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="8911a-195">**gllight**</span><span class="sxs-lookup"><span data-stu-id="8911a-195">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="8911a-196">**gllightmodel**</span><span class="sxs-lookup"><span data-stu-id="8911a-196">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





