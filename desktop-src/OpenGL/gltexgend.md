---
title: gltexgend-Funktion (GL. h)
description: Steuert die Generierung von Texturkoordinaten. | gltexgend-Funktion (GL. h)
ms.assetid: 75ab3468-281d-4c8d-95cc-138d75646cdf
keywords:
- gltexgend-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexGend
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45854eb1e2070f334bfc906c249fbb4341ab74d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104558761"
---
# <a name="gltexgend-function"></a><span data-ttu-id="637bb-105">gltexgend-Funktion</span><span class="sxs-lookup"><span data-stu-id="637bb-105">glTexGend function</span></span>

<span data-ttu-id="637bb-106">Steuert die Generierung von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="637bb-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="637bb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="637bb-107">Syntax</span></span>


```C++
void WINAPI glTexGend(
   GLenum   coord,
   GLenum   pname,
   GLdouble param
);
```



## <a name="parameters"></a><span data-ttu-id="637bb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="637bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="637bb-109">*Koord*</span><span class="sxs-lookup"><span data-stu-id="637bb-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="637bb-110">Eine Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="637bb-110">A texture coordinate.</span></span> <span data-ttu-id="637bb-111">Muss eines der folgenden sein: GL \_ S, GL \_ T, GL \_ R oder GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="637bb-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="637bb-112">**pName**</span><span class="sxs-lookup"><span data-stu-id="637bb-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="637bb-113">Der symbolische Name der Texturkoordinaten Generierungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="637bb-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="637bb-114">*param*</span><span class="sxs-lookup"><span data-stu-id="637bb-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="637bb-115">Ein einwertiger Parameter für die Textur Generierung, eines von GL- \_ Objekt \_ linear, GL \_ Eye \_ linear oder GL \_ Sphere \_ map.</span><span class="sxs-lookup"><span data-stu-id="637bb-115">A single valued texture generation parameter, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="637bb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="637bb-116">Return value</span></span>

<span data-ttu-id="637bb-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="637bb-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="637bb-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="637bb-118">Error codes</span></span>

<span data-ttu-id="637bb-119">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="637bb-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="637bb-120">Name</span><span class="sxs-lookup"><span data-stu-id="637bb-120">Name</span></span>                                                                                                  | <span data-ttu-id="637bb-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="637bb-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="637bb-122"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="637bb-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="637bb-123">*coord* oder *PName* war kein akzeptierter definierter Wert, oder *PName* war der \_ GL \_ -Textur gen \_ -Modus, und der Parameter war kein akzeptierter definierter Wert. </span><span class="sxs-lookup"><span data-stu-id="637bb-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="637bb-124"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="637bb-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="637bb-125">*PName* war der \_ GL \_ -Textur gen \_ -Modus, die Parameter "GL  \_ Sphere Map" und " \_ *coord* " war "GL \_ R" oder "GL \_ Q".</span><span class="sxs-lookup"><span data-stu-id="637bb-125">*pname* was GL\_TEXTURE\_GEN\_MODE, *params* was GL\_SPHERE\_MAP, and *coord* was either GL\_R or GL\_Q</span></span><br/>                                     |
| <dl> <span data-ttu-id="637bb-126"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="637bb-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="637bb-127">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="637bb-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="637bb-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="637bb-128">Remarks</span></span>

<span data-ttu-id="637bb-129">Die **gltexgen** -Funktion wählt eine Texturkoordinaten-Generierungs Funktion aus oder liefert Koeffizienten für eine der Funktionen.</span><span class="sxs-lookup"><span data-stu-id="637bb-129">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="637bb-130">Der *coord* -Parameter benennt eine der (s, t, r, q)-Texturkoordinaten und muss eines der folgenden Symbole sein: GL \_ s, GL \_ t, GL \_ r oder GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="637bb-130">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="637bb-131">Der *PName* -Parameter muss eine von drei symbolischen Konstanten sein: GL \_ Texture \_ gen- \_ Modus, GL- \_ Objekt \_ Ebene oder GL- \_ Eye- \_ Ebene.</span><span class="sxs-lookup"><span data-stu-id="637bb-131">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="637bb-132">Wenn " *PName* " der GL- \_ Textur \_ gen-Modus ist \_ , gibt *param* einen Modus, eines von GL- \_ Objekt \_ linear, GL \_ Eye \_ linear oder eine GL- \_ Kugel Karte an \_ .</span><span class="sxs-lookup"><span data-stu-id="637bb-132">If *pname* is GL\_TEXTURE\_GEN\_MODE, then *param* specifies a mode, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span> <span data-ttu-id="637bb-133">Wenn *PName* entweder eine GL- \_ Objekt \_ Ebene oder \_ eine GL-Augen Ebene ist \_ , enthält *param* Koeffizienten für die entsprechende Textur Generierungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="637bb-133">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="637bb-134">Wenn die Textur Generierungs Funktion ein GL- \_ Objekt \_ linear ist, wird die Funktion</span><span class="sxs-lookup"><span data-stu-id="637bb-134">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

![Gleichung, die die gltexgen-Funktion anzeigt, wenn die Textur Generierungs Funktion GL_OBJECT_LINEAR ist.](images/tex02.png)

<span data-ttu-id="637bb-136">wird verwendet, wobei g der Wert ist, der für die in coord benannte Koordinate berechnet wird. P1, P2, P3 und P4 sind die vier Werte, die in Parametern bereitgestellt werden. und x?, y?, z? und w? die Objekt Koordinaten des Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="637bb-136">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="637bb-137">Sie können diese Funktion verwenden, um das Gelände mithilfe der Meeres Ebene als Bezugs Ebene (definiert durch P1, P2, P3 und P4) zu strukturieren.</span><span class="sxs-lookup"><span data-stu-id="637bb-137">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="637bb-138">Die Funktion für die \_ \_ lineare Koordinaten Generierung von GL-Objekten berechnet die Höhe eines Gelände Scheitel Punkts als Abstand von der Meeres Ebene. diese Höhe wird zum Indizieren des Textur Bilds verwendet, um die Spitzen und das grüne Gras zum Rand zu ordnen.</span><span class="sxs-lookup"><span data-stu-id="637bb-138">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="637bb-139">Wenn die Textur Generierungs Funktion "GL \_ Eye linear" ist \_ , wird die Funktion</span><span class="sxs-lookup"><span data-stu-id="637bb-139">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

![Gleichung, die die gltexgen-Funktion anzeigt, wenn die Textur Generierungs Funktion GL_EYE_LINEAR ist.](images/tex02.png)

<span data-ttu-id="637bb-141">wird verwendet, wobei</span><span class="sxs-lookup"><span data-stu-id="637bb-141">is used, where</span></span>

![Gleichung, die die Augen Koordinaten des Scheitel Punkts anzeigt.](images/tex03.png)

<span data-ttu-id="637bb-143">und x?, y?, z? und w? die Augen Koordinaten des Scheitel Punkts, P1, P2, P3 und P4 sind die Werte, die in *param* angegeben werden, und M ist die Modelview-Matrix, wenn Sie **gltexgen** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="637bb-143">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="637bb-144">Wenn M unzureichend bedingt oder Singular ist, können die von der resultierenden Funktion generierten Texturkoordinaten ungenau oder undefiniert sein.</span><span class="sxs-lookup"><span data-stu-id="637bb-144">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="637bb-145">Mit den Werten in *param* wird eine Verweis Ebene in den Augen Koordinaten definiert.</span><span class="sxs-lookup"><span data-stu-id="637bb-145">The values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="637bb-146">Die auf Sie angewendete Modelview-Matrix darf nicht identisch sein, wenn die Polygon Scheitel Punkte transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="637bb-146">The modelview matrix that is applied to them cannot be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="637bb-147">Diese Funktion legt ein Feld von Texturkoordinaten fest, das dynamische Konturlinien für das Verschieben von Objekten erzeugt.</span><span class="sxs-lookup"><span data-stu-id="637bb-147">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="637bb-148">Wenn " *PName* " den Wert "GL \_ Sphere \_ map" und " *coord* " entweder "GL \_ s" oder "GL t" ist \_ , werden die S-und T-Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="637bb-148">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="637bb-149">U. a. der Einheits Vektor, der vom Ursprung auf den Polygon Scheitelpunkt zeigt (in Augen Koordinaten).</span><span class="sxs-lookup"><span data-stu-id="637bb-149">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="637bb-150">Let n ist die aktuelle normale, nach der Transformation zu den Augen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="637bb-150">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="637bb-151">Let f = (FX () fy () FZ) T der reflektionvektor, damit</span><span class="sxs-lookup"><span data-stu-id="637bb-151">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Gleichung, die den Reflektionsvektor als Funktion des Einheits Vektors und des aktuellen normalen anzeigt.](images/tex05.png)

<span data-ttu-id="637bb-153">Und schließlich</span><span class="sxs-lookup"><span data-stu-id="637bb-153">Finally, let</span></span>

![Gleichung, die m als Funktion des reflektionsvektors anzeigt.](images/tex07.png)

<span data-ttu-id="637bb-155">Dann sind die den i-und t-Texturkoordinaten zugewiesenen Werte</span><span class="sxs-lookup"><span data-stu-id="637bb-155">Then the values assigned to the i and t texture coordinates are</span></span>

![Gleichung, die den i-und t-Texturkoordinaten zugewiesene Werte anzeigt.](images/tex06.png)

<span data-ttu-id="637bb-157">Sie können eine Texturkoordinaten-Generierungs Funktion aktivieren oder deaktivieren, indem Sie [**glEnable**](glenable.md) oder [**gldeaktivieren**](gldisable.md) mit einem der symbolischen Texturkoordinaten Namen (GL \_ Texture \_ gen \_ S, GL \_ Texture \_ gen \_ T, GL \_ Texture \_ gen \_ R oder GL \_ Texture \_ gen \_ Q) als Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="637bb-157">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="637bb-158">Wenn diese Funktion aktiviert ist, wird die angegebene Textur Koordinate entsprechend der der Koordinate zugeordneten Generierungs Funktion berechnet.</span><span class="sxs-lookup"><span data-stu-id="637bb-158">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="637bb-159">Wenn die Funktion deaktiviert ist, nehmen nachfolgende Vertices die angegebene Textur Koordinate aus dem aktuellen Satz von Texturkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="637bb-159">When the function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="637bb-160">Anfänglich werden alle Textur Generierungs Funktionen auf "GL Eye linear" festgelegt \_ \_ und sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="637bb-160">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="637bb-161">Beide s-Ebenen-Gleichungen sind (1, 0, 0, 0); Beide t-Ebenen-Gleichungen sind (0, 1, 0, 0); und alle Gleichungen der r-und q-Ebene sind (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="637bb-161">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="637bb-162">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit gltexgen abgerufen:</span><span class="sxs-lookup"><span data-stu-id="637bb-162">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="637bb-163">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="637bb-163">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="637bb-164">[**glisenabled**](glisenabled.md) mit Argument GL \_ Textur \_ gen \_ S</span><span class="sxs-lookup"><span data-stu-id="637bb-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="637bb-165">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="637bb-165">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="637bb-166">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="637bb-166">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="637bb-167">[**glisenabled**](glisenabled.md) mit Argument GL \_ Textur \_ gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="637bb-167">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="637bb-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="637bb-168">Requirements</span></span>



| <span data-ttu-id="637bb-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="637bb-169">Requirement</span></span> | <span data-ttu-id="637bb-170">Wert</span><span class="sxs-lookup"><span data-stu-id="637bb-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="637bb-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="637bb-171">Minimum supported client</span></span><br/> | <span data-ttu-id="637bb-172">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="637bb-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="637bb-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="637bb-173">Minimum supported server</span></span><br/> | <span data-ttu-id="637bb-174">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="637bb-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="637bb-175">Header</span><span class="sxs-lookup"><span data-stu-id="637bb-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="637bb-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="637bb-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="637bb-177">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="637bb-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="637bb-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="637bb-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="637bb-179">DLL</span><span class="sxs-lookup"><span data-stu-id="637bb-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="637bb-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="637bb-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="637bb-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="637bb-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637bb-182">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="637bb-182">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="637bb-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="637bb-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="637bb-184">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="637bb-184">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="637bb-185">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="637bb-185">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="637bb-186">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="637bb-186">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="637bb-187">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="637bb-187">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="637bb-188">**gltexd**</span><span class="sxs-lookup"><span data-stu-id="637bb-188">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="637bb-189">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="637bb-189">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="637bb-190">**gltexparameter**</span><span class="sxs-lookup"><span data-stu-id="637bb-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="637bb-191">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="637bb-191">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="637bb-192">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="637bb-192">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





