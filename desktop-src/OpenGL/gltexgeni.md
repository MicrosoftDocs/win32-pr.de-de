---
title: gltexgeni-Funktion (GL. h)
description: Steuert die Generierung von Texturkoordinaten. | gltexgeni-Funktion (GL. h)
ms.assetid: beffcb24-c99b-4b2a-a9c3-2c2cc1afe5e5
keywords:
- gltexgeni-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexGeni
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20bb1121a8f125f06bf8e6e18f56c96fbeeb692d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104557990"
---
# <a name="gltexgeni-function"></a><span data-ttu-id="cf7f3-105">gltexgeni-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf7f3-105">glTexGeni function</span></span>

<span data-ttu-id="cf7f3-106">Steuert die Generierung von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf7f3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf7f3-107">Syntax</span></span>


```C++
void WINAPI glTexGeni(
   GLenum coord,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="cf7f3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf7f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7f3-109">*Koord*</span><span class="sxs-lookup"><span data-stu-id="cf7f3-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="cf7f3-110">Eine Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-110">A texture coordinate.</span></span> <span data-ttu-id="cf7f3-111">Muss eines der folgenden sein: GL \_ S, GL \_ T, GL \_ R oder GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="cf7f3-112">**pName**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="cf7f3-113">Der symbolische Name der Texturkoordinaten Generierungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="cf7f3-114">*param*</span><span class="sxs-lookup"><span data-stu-id="cf7f3-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="cf7f3-115">Ein einwertiger Parameter für die Textur Generierung, eines von GL- \_ Objekt \_ linear, GL \_ Eye \_ linear oder GL \_ Sphere \_ map.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-115">A single valued texture generation parameter, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf7f3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf7f3-116">Return value</span></span>

<span data-ttu-id="cf7f3-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cf7f3-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cf7f3-118">Error codes</span></span>

<span data-ttu-id="cf7f3-119">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cf7f3-120">Name</span><span class="sxs-lookup"><span data-stu-id="cf7f3-120">Name</span></span>                                                                                                  | <span data-ttu-id="cf7f3-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cf7f3-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf7f3-122"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf7f3-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cf7f3-123">*coord* oder *PName* war kein akzeptierter definierter Wert, oder *PName* war der \_ GL \_ -Textur gen \_ -Modus, und der Parameter war kein akzeptierter definierter Wert. </span><span class="sxs-lookup"><span data-stu-id="cf7f3-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="cf7f3-124"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf7f3-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cf7f3-125">*PName* war der \_ GL \_ -Textur gen \_ -Modus, die Parameter "GL  \_ Sphere Map" und " \_ *coord* " war "GL \_ R" oder "GL \_ Q".</span><span class="sxs-lookup"><span data-stu-id="cf7f3-125">*pname* was GL\_TEXTURE\_GEN\_MODE, *params* was GL\_SPHERE\_MAP, and *coord* was either GL\_R or GL\_Q</span></span><br/>                                     |
| <dl> <span data-ttu-id="cf7f3-126"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="cf7f3-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cf7f3-127">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="cf7f3-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf7f3-128">Remarks</span></span>

<span data-ttu-id="cf7f3-129">Die **gltexgen** -Funktion wählt eine Texturkoordinaten-Generierungs Funktion aus oder liefert Koeffizienten für eine der Funktionen.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-129">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="cf7f3-130">Der *coord* -Parameter benennt eine der (s, t, r, q)-Texturkoordinaten und muss eines der folgenden Symbole sein: GL \_ s, GL \_ t, GL \_ r oder GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-130">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="cf7f3-131">Der *PName* -Parameter muss eine von drei symbolischen Konstanten sein: GL \_ Texture \_ gen- \_ Modus, GL- \_ Objekt \_ Ebene oder GL- \_ Eye- \_ Ebene.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-131">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="cf7f3-132">Wenn " *PName* " der GL- \_ Textur \_ gen-Modus ist \_ , gibt *param* einen Modus, eines von GL- \_ Objekt \_ linear, GL \_ Eye \_ linear oder eine GL- \_ Kugel Karte an \_ .</span><span class="sxs-lookup"><span data-stu-id="cf7f3-132">If *pname* is GL\_TEXTURE\_GEN\_MODE, then *param* specifies a mode, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span> <span data-ttu-id="cf7f3-133">Wenn *PName* entweder eine GL- \_ Objekt \_ Ebene oder \_ eine GL-Augen Ebene ist \_ , enthält *param* Koeffizienten für die entsprechende Textur Generierungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-133">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="cf7f3-134">Wenn die Textur Generierungs Funktion ein GL- \_ Objekt \_ linear ist, wird die Funktion</span><span class="sxs-lookup"><span data-stu-id="cf7f3-134">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="cf7f3-135">! [Gleichung, die die gltexgen-Funktion anzeigt, wenn die Textur Generierungs Funktion GL_OBJECT_LINEAR ist.]</span><span class="sxs-lookup"><span data-stu-id="cf7f3-135">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="cf7f3-136">wird verwendet, wobei g der Wert ist, der für die in coord benannte Koordinate berechnet wird. P1, P2, P3 und P4 sind die vier Werte, die in Parametern bereitgestellt werden. und x?, y?, z? und w? die Objekt Koordinaten des Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-136">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="cf7f3-137">Sie können diese Funktion verwenden, um das Gelände mithilfe der Meeres Ebene als Bezugs Ebene (definiert durch P1, P2, P3 und P4) zu strukturieren.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-137">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="cf7f3-138">Die Funktion für die \_ \_ lineare Koordinaten Generierung von GL-Objekten berechnet die Höhe eines Gelände Scheitel Punkts als Abstand von der Meeres Ebene. diese Höhe wird zum Indizieren des Textur Bilds verwendet, um die Spitzen und das grüne Gras zum Rand zu ordnen.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-138">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="cf7f3-139">Wenn die Textur Generierungs Funktion "GL \_ Eye linear" ist \_ , wird die Funktion</span><span class="sxs-lookup"><span data-stu-id="cf7f3-139">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="cf7f3-140">! [Gleichung, die die gltexgen-Funktion anzeigt, wenn die Textur Generierungs Funktion GL_EYE_LINEAR ist.]</span><span class="sxs-lookup"><span data-stu-id="cf7f3-140">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="cf7f3-141">wird verwendet, wobei</span><span class="sxs-lookup"><span data-stu-id="cf7f3-141">is used, where</span></span>

![Gleichung, die die Augen Koordinaten des Scheitel Punkts anzeigt.](images/tex03.png)

<span data-ttu-id="cf7f3-143">und x?, y?, z? und w? die Augen Koordinaten des Scheitel Punkts, P1, P2, P3 und P4 sind die Werte, die in *param* angegeben werden, und M ist die Modelview-Matrix, wenn Sie **gltexgen** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-143">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="cf7f3-144">Wenn M unzureichend bedingt oder Singular ist, können die von der resultierenden Funktion generierten Texturkoordinaten ungenau oder undefiniert sein.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-144">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="cf7f3-145">Beachten Sie, dass die Werte in *param* eine Verweis Ebene in den Augen Koordinaten definieren.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-145">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="cf7f3-146">Die Modelview-Matrix, die auf Sie angewendet wird, ist möglicherweise nicht identisch, wenn die Polygon Scheitel Punkte transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-146">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="cf7f3-147">Diese Funktion legt ein Feld von Texturkoordinaten fest, das dynamische Konturlinien für das Verschieben von Objekten erzeugt.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-147">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="cf7f3-148">Wenn " *PName* " den Wert "GL \_ Sphere \_ map" und " *coord* " entweder "GL \_ s" oder "GL t" ist \_ , werden die S-und T-Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="cf7f3-148">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="cf7f3-149">U. a. der Einheits Vektor, der vom Ursprung auf den Polygon Scheitelpunkt zeigt (in Augen Koordinaten).</span><span class="sxs-lookup"><span data-stu-id="cf7f3-149">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="cf7f3-150">Let n ist die aktuelle normale, nach der Transformation zu den Augen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-150">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="cf7f3-151">Let f = (FX () fy () FZ) T der reflektionvektor, damit</span><span class="sxs-lookup"><span data-stu-id="cf7f3-151">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Gleichung, die den Reflektionsvektor als Funktion des Einheits Vektors und des aktuellen normalen anzeigt.](images/tex05.png)

<span data-ttu-id="cf7f3-153">Und schließlich</span><span class="sxs-lookup"><span data-stu-id="cf7f3-153">Finally, let</span></span>

![Gleichung, die m als Funktion des reflektionsvektors anzeigt.](images/tex07.png)

<span data-ttu-id="cf7f3-155">Dann sind die den i-und t-Texturkoordinaten zugewiesenen Werte</span><span class="sxs-lookup"><span data-stu-id="cf7f3-155">Then the values assigned to the i and t texture coordinates are</span></span>

![Gleichung, die den i-und t-Texturkoordinaten zugewiesene Werte anzeigt.](images/tex06.png)

<span data-ttu-id="cf7f3-157">Sie können eine Texturkoordinaten-Generierungs Funktion aktivieren oder deaktivieren, indem Sie [**glEnable**](glenable.md) oder [**gldeaktivieren**](gldisable.md) mit einem der symbolischen Texturkoordinaten Namen (GL \_ Texture \_ gen \_ S, GL \_ Texture \_ gen \_ T, GL \_ Texture \_ gen \_ R oder GL \_ Texture \_ gen \_ Q) als Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-157">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="cf7f3-158">Wenn diese Funktion aktiviert ist, wird die angegebene Textur Koordinate entsprechend der der Koordinate zugeordneten Generierungs Funktion berechnet.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-158">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="cf7f3-159">Wenn diese Funktion deaktiviert ist, nehmen nachfolgende Vertices die angegebene Textur Koordinate aus dem aktuellen Satz von Texturkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-159">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="cf7f3-160">Anfänglich werden alle Textur Generierungs Funktionen auf "GL Eye linear" festgelegt \_ \_ und sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-160">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="cf7f3-161">Beide s-Ebenen-Gleichungen sind (1, 0, 0, 0); Beide t-Ebenen-Gleichungen sind (0, 1, 0, 0); und alle Gleichungen der r-und q-Ebene sind (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="cf7f3-161">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="cf7f3-162">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit gltexgen abgerufen:</span><span class="sxs-lookup"><span data-stu-id="cf7f3-162">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="cf7f3-163">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-163">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="cf7f3-164">[**glisenabled**](glisenabled.md) mit Argument GL \_ Textur \_ gen \_ S</span><span class="sxs-lookup"><span data-stu-id="cf7f3-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="cf7f3-165">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="cf7f3-165">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="cf7f3-166">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Textur \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="cf7f3-166">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="cf7f3-167">[**glisenabled**](glisenabled.md) mit Argument GL \_ Textur \_ gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="cf7f3-167">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="cf7f3-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf7f3-168">Requirements</span></span>



| <span data-ttu-id="cf7f3-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf7f3-169">Requirement</span></span> | <span data-ttu-id="cf7f3-170">Wert</span><span class="sxs-lookup"><span data-stu-id="cf7f3-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7f3-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf7f3-171">Minimum supported client</span></span><br/> | <span data-ttu-id="cf7f3-172">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf7f3-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cf7f3-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf7f3-173">Minimum supported server</span></span><br/> | <span data-ttu-id="cf7f3-174">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf7f3-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf7f3-175">Header</span><span class="sxs-lookup"><span data-stu-id="cf7f3-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf7f3-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf7f3-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cf7f3-177">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf7f3-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf7f3-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf7f3-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf7f3-179">DLL</span><span class="sxs-lookup"><span data-stu-id="cf7f3-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf7f3-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf7f3-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf7f3-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf7f3-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7f3-182">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-182">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-184">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-184">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-185">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-185">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-186">**glgettexgen**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-186">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-187">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-187">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-188">gltexd</span><span class="sxs-lookup"><span data-stu-id="cf7f3-188">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-189">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-189">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-190">gltexparameter</span><span class="sxs-lookup"><span data-stu-id="cf7f3-190">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-191">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-191">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-192">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-192">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





