---
title: gltexgeniv-Funktion (GL. h)
description: Steuert die Generierung von Texturkoordinaten. | gltexgeniv-Funktion (GL. h)
ms.assetid: e95f2844-414a-4fb2-944e-4d0b6e51bdd2
keywords:
- gltexgeniv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexGeniv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05a5981e76c44ea8ee0fe037ac5c28d8c45f5f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104570801"
---
# <a name="gltexgeniv-function"></a><span data-ttu-id="b3397-105">gltexgeniv-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3397-105">glTexGeniv function</span></span>

<span data-ttu-id="b3397-106">Steuert die Generierung von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="b3397-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3397-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3397-107">Syntax</span></span>


```C++
void WINAPI glTexGeniv(
         GLenum coord,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="b3397-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3397-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3397-109">*Koord*</span><span class="sxs-lookup"><span data-stu-id="b3397-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="b3397-110">Eine Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="b3397-110">A texture coordinate.</span></span> <span data-ttu-id="b3397-111">Muss eines der folgenden sein: GL \_ S, GL \_ T, GL \_ R oder GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="b3397-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="b3397-112">**pName**</span><span class="sxs-lookup"><span data-stu-id="b3397-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="b3397-113">Der symbolische Name der Texturkoordinaten Generierungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="b3397-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="b3397-114">*params*</span><span class="sxs-lookup"><span data-stu-id="b3397-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b3397-115">Ein Array, das die Koeffizienten für die entsprechende Textur Generierungs Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="b3397-115">An array that contains the coefficients for the corresponding texture generation function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3397-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3397-116">Return value</span></span>

<span data-ttu-id="b3397-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b3397-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3397-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b3397-118">Error codes</span></span>

<span data-ttu-id="b3397-119">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b3397-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b3397-120">Name</span><span class="sxs-lookup"><span data-stu-id="b3397-120">Name</span></span>                                                                                                  | <span data-ttu-id="b3397-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b3397-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3397-122"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3397-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b3397-123">*coord* oder *PName* war kein akzeptierter definierter Wert, oder *PName* war der \_ GL \_ -Textur gen \_ -Modus, und der Parameter war kein akzeptierter definierter Wert. </span><span class="sxs-lookup"><span data-stu-id="b3397-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="b3397-124"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b3397-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b3397-125">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b3397-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="b3397-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3397-126">Remarks</span></span>

<span data-ttu-id="b3397-127">Die **gltexgen** -Funktion wählt eine Texturkoordinaten-Generierungs Funktion aus oder liefert Koeffizienten für eine der Funktionen.</span><span class="sxs-lookup"><span data-stu-id="b3397-127">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="b3397-128">Der *coord* -Parameter benennt eine der (s, t, r, q)-Texturkoordinaten und muss eines der folgenden Symbole sein: GL \_ s, GL \_ t, GL \_ r oder GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="b3397-128">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="b3397-129">Der *PName* -Parameter muss eine von drei symbolischen Konstanten sein: GL \_ Texture \_ gen- \_ Modus, GL- \_ Objekt \_ Ebene oder GL- \_ Eye- \_ Ebene.</span><span class="sxs-lookup"><span data-stu-id="b3397-129">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="b3397-130">Wenn *PName* entweder eine GL- \_ Objekt \_ Ebene oder \_ eine GL-Augen Ebene ist \_ , enthält *param* Koeffizienten für die entsprechende Textur Generierungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="b3397-130">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="b3397-131">Wenn die Textur Generierungs Funktion ein GL- \_ Objekt \_ linear ist, wird die Funktion</span><span class="sxs-lookup"><span data-stu-id="b3397-131">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="b3397-132">! [Gleichung, die die gltexgen-Funktion anzeigt, wenn die Textur Generierungs Funktion GL_OBJECT_LINEAR ist.]</span><span class="sxs-lookup"><span data-stu-id="b3397-132">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="b3397-133">wird verwendet, wobei g der Wert ist, der für die in coord benannte Koordinate berechnet wird. P1, P2, P3 und P4 sind die vier Werte, die in Parametern bereitgestellt werden. und x?, y?, z? und w? die Objekt Koordinaten des Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="b3397-133">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="b3397-134">Sie können diese Funktion verwenden, um das Gelände mithilfe der Meeres Ebene als Bezugs Ebene (definiert durch P1, P2, P3 und P4) zu strukturieren.</span><span class="sxs-lookup"><span data-stu-id="b3397-134">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="b3397-135">Die Funktion für die \_ \_ lineare Koordinaten Generierung von GL-Objekten berechnet die Höhe eines Gelände Scheitel Punkts als Abstand von der Meeres Ebene. diese Höhe wird zum Indizieren des Textur Bilds verwendet, um die Spitzen und das grüne Gras zum Rand zu ordnen.</span><span class="sxs-lookup"><span data-stu-id="b3397-135">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="b3397-136">Wenn die Textur Generierungs Funktion "GL \_ Eye linear" ist \_ , wird die Funktion</span><span class="sxs-lookup"><span data-stu-id="b3397-136">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="b3397-137">! [Gleichung, die die gltexgen-Funktion anzeigt, wenn die Textur Generierungs Funktion GL_EYE_LINEAR ist.]</span><span class="sxs-lookup"><span data-stu-id="b3397-137">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="b3397-138">wird verwendet, wobei</span><span class="sxs-lookup"><span data-stu-id="b3397-138">is used, where</span></span>

![Gleichung, die die Augen Koordinaten des Scheitel Punkts anzeigt.](images/tex03.png)

<span data-ttu-id="b3397-140">und x?, y?, z? und w? die Augen Koordinaten des Scheitel Punkts, P1, P2, P3 und P4 sind die Werte, die in *param* angegeben werden, und M ist die Modelview-Matrix, wenn Sie **gltexgen** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b3397-140">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="b3397-141">Wenn M unzureichend bedingt oder Singular ist, können die von der resultierenden Funktion generierten Texturkoordinaten ungenau oder undefiniert sein.</span><span class="sxs-lookup"><span data-stu-id="b3397-141">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="b3397-142">Beachten Sie, dass die Werte in *param* eine Verweis Ebene in den Augen Koordinaten definieren.</span><span class="sxs-lookup"><span data-stu-id="b3397-142">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="b3397-143">Die Modelview-Matrix, die auf Sie angewendet wird, ist möglicherweise nicht identisch, wenn die Polygon Scheitel Punkte transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="b3397-143">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="b3397-144">Diese Funktion legt ein Feld von Texturkoordinaten fest, das dynamische Konturlinien für das Verschieben von Objekten erzeugt.</span><span class="sxs-lookup"><span data-stu-id="b3397-144">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="b3397-145">Wenn " *PName* " den Wert "GL \_ Sphere \_ map" und " *coord* " entweder "GL \_ s" oder "GL t" ist \_ , werden die S-und T-Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="b3397-145">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="b3397-146">U. a. der Einheits Vektor, der vom Ursprung auf den Polygon Scheitelpunkt zeigt (in Augen Koordinaten).</span><span class="sxs-lookup"><span data-stu-id="b3397-146">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="b3397-147">Let n ist die aktuelle normale, nach der Transformation zu den Augen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="b3397-147">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="b3397-148">Let f = (FX () fy () FZ) T der reflektionvektor, damit</span><span class="sxs-lookup"><span data-stu-id="b3397-148">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Gleichung, die den Reflektionsvektor als Funktion des Einheits Vektors und des aktuellen normalen anzeigt.](images/tex05.png)

<span data-ttu-id="b3397-150">Und schließlich</span><span class="sxs-lookup"><span data-stu-id="b3397-150">Finally, let</span></span>

![Gleichung, die m als Funktion des reflektionsvektors anzeigt.](images/tex07.png)

<span data-ttu-id="b3397-152">Dann sind die den i-und t-Texturkoordinaten zugewiesenen Werte</span><span class="sxs-lookup"><span data-stu-id="b3397-152">Then the values assigned to the i and t texture coordinates are</span></span>

![Gleichung, die den i-und t-Texturkoordinaten zugewiesene Werte anzeigt.](images/tex06.png)

<span data-ttu-id="b3397-154">Sie können eine Texturkoordinaten-Generierungs Funktion aktivieren oder deaktivieren, indem Sie [**glEnable**](glenable.md) oder [**gldeaktivieren**](gldisable.md) mit einem der symbolischen Texturkoordinaten Namen (GL \_ Texture \_ gen \_ S, GL \_ Texture \_ gen \_ T, GL \_ Texture \_ gen \_ R oder GL \_ Texture \_ gen \_ Q) als Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3397-154">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="b3397-155">Wenn diese Funktion aktiviert ist, wird die angegebene Textur Koordinate entsprechend der der Koordinate zugeordneten Generierungs Funktion berechnet.</span><span class="sxs-lookup"><span data-stu-id="b3397-155">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="b3397-156">Wenn diese Funktion deaktiviert ist, nehmen nachfolgende Vertices die angegebene Textur Koordinate aus dem aktuellen Satz von Texturkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="b3397-156">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="b3397-157">Anfänglich werden alle Textur Generierungs Funktionen auf "GL Eye linear" festgelegt \_ \_ und sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b3397-157">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="b3397-158">Beide s-Ebenen-Gleichungen sind (1, 0, 0, 0); Beide t-Ebenen-Gleichungen sind (0, 1, 0, 0); und alle Gleichungen der r-und q-Ebene sind (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="b3397-158">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="b3397-159">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit gltexgen abgerufen:</span><span class="sxs-lookup"><span data-stu-id="b3397-159">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="b3397-160">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="b3397-160">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="b3397-161">[**glisenabled**](glisenabled.md) mit Argument GL \_ Textur \_ gen \_ S</span><span class="sxs-lookup"><span data-stu-id="b3397-161">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="b3397-162">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="b3397-162">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="b3397-163">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="b3397-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="b3397-164">[**glisenabled**](glisenabled.md) mit Argument GL \_ Textur \_ gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="b3397-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="b3397-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3397-165">Requirements</span></span>



| <span data-ttu-id="b3397-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3397-166">Requirement</span></span> | <span data-ttu-id="b3397-167">Wert</span><span class="sxs-lookup"><span data-stu-id="b3397-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3397-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3397-168">Minimum supported client</span></span><br/> | <span data-ttu-id="b3397-169">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3397-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3397-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3397-170">Minimum supported server</span></span><br/> | <span data-ttu-id="b3397-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3397-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3397-172">Header</span><span class="sxs-lookup"><span data-stu-id="b3397-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3397-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3397-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b3397-174">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3397-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3397-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3397-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3397-176">DLL</span><span class="sxs-lookup"><span data-stu-id="b3397-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3397-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3397-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3397-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3397-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3397-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b3397-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b3397-180">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b3397-180">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b3397-181">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b3397-181">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b3397-182">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="b3397-182">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="b3397-183">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="b3397-183">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="b3397-184">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="b3397-184">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="b3397-185">gltexd</span><span class="sxs-lookup"><span data-stu-id="b3397-185">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="b3397-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b3397-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b3397-187">gltexparameter</span><span class="sxs-lookup"><span data-stu-id="b3397-187">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="b3397-188">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="b3397-188">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="b3397-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="b3397-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





