---
title: glPushAttrib-Funktion (Gl.h)
description: Pusht den Attributstapel.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- glPushAttrib-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252859065ddae0439441acb6afd797d26bbed44a246b628b4f0350d7f3b1e2d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519990"
---
# <a name="glpushattrib-function"></a>glPushAttrib-Funktion

Pusht den Attributstapel.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mask* 
</dt> <dd>

Eine Maske, die angibt, welche Attribute zu speichern sind. Die konstanten symbolischen Masken und deren zugeordneter OpenGL-Zustand lauten wie folgt (die eingerückten Absätze listen auf, welche Attribute gespeichert werden):

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>\_ \_ GL-PUFFERBIT \_ 
</dt> <dd>

Klarwert des Akkumulationspuffers

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL \_ COLOR \_ BUFFER \_ BIT
</dt> <dd>

GL \_ ALPHA TEST enable \_ bit

Alphatestfunktion und Verweiswert

GL \_ BLEND enable bit

Mischen von Quell- und Zielfunktionen

GL \_ DITHER enable bit

GL \_ DRAW \_ BUFFER-Einstellung

GL \_ LOGIC OP enable \_ bit

Logic Op-Funktion

Löschen von Werten im Farbmodus und Indexmodus

Farbmodus- und Indexmodus-Schreibmasken

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL \_ CURRENT \_ BIT
</dt> <dd>

Aktuelle RGBA-Farbe

Aktueller Farbindex

Aktueller normaler Vektor

Aktuelle Texturkoordinaten

Aktuelle Rasterposition GL \_ CURRENT RASTER POSITION VALID \_ \_ \_ flag

RGBA-Farbe, die der aktuellen Rasterposition zugeordnet ist

Farbindex, der der aktuellen Rasterposition zugeordnet ist

Texturkoordinaten, die der aktuellen Rasterposition zugeordnet sind

GL \_ \_ EDGE-FLAG-Flag

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL \_ DEPTH \_ BUFFER \_ BIT
</dt> <dd>

GL \_ DEPTH TEST enable \_ bit

Tiefenpuffertestfunktion

Tiefenpuffer– eindeutiger Wert

GL \_ DEPTH \_ WRITEMASK enable bit

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL \_ ENABLE \_ BIT
</dt> <dd>

GL \_ ALPHA \_ TEST-Flag

GL \_ AUTO \_ NORMAL-Flag

GL \_ BLEND-Flag

Aktivieren von Bits für die benutzerdefinierbaren Clippingebenen

\_ \_ GL-FARBMATERIAL

GL \_ CULL \_ FACE-Flag

GL \_ DEPTH \_ TEST-Flag

GL \_ DITHER-Flag

GL \_ GL GL-FLAG

GL \_ LIGHT *i* where 0 <= *i* < GL \_ MAX \_ LIGHTS

GL \_ LIGHTING-Flag

GL \_ LINE \_ SMOOTH-Flag

GL \_ LINE \_ STIPPLE-Flag

GL \_ COLOR \_ LOGIC \_ OP-Flag

GL \_ INDEX \_ LOGIC \_ OP-Flag

GL \_ MAP1 \_ x, wobei x ein Kartentyp ist

GL \_ MAP2 \_ x, wobei x ein Kartentyp ist

GL \_ NORMALIZE-Flag

GL \_ POINT \_ SMOOTH-Flag

GL \_ POLYGON \_ OFFSET \_ LINE-Flag

GL \_ POLYGON \_ OFFSET \_ FILL-Flag

GL \_ POLYGON \_ OFFSET \_ POINT-Flag

GL \_ POLYGON \_ SMOOTH-Flag

GL \_ POLYGON \_ STIPPLE-Flag

GL \_ SCISSOR \_ TEST-Flag

\_ \_ GL-STENCIL-TESTflag

GL \_ TEXTURE \_ 1D-Flag

GL \_ TEXTURE \_ 2D-Flag

Kennzeichnet GL \_ TEXTURE \_ GEN \_ x, wobei x "S", "T", "R" oder "Q" ist

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL \_ EVAL \_ BIT
</dt> <dd>

GL \_ MAP1 \_ x aktiviert Bits, wobei x ein Kartentyp ist

GL \_ MAP2 \_ x enable bits, wobei x ein Kartentyp ist

1D-Rasterendpunkte und -divisionen

2D-Rasterendpunkte und -divisionen

GL \_ AUTO NORMAL enable \_ bit

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL \_ \_ GL-BIT
</dt> <dd>

GL \_ OHNE AKTIVIERUNGsflag

Farbe des Farbtons "Farbton

Dichte von 50000

Linearer Linearer Start

Lineares Ende

Index "Index"

\_GL-WERT FÜR \_ DEN GL-MODUS

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL \_ HINT \_ BIT
</dt> <dd>

GL \_ PERSPECTIVE \_ CORRECTION \_ HINT-Einstellung

GL \_ POINT \_ SMOOTH \_ HINT-Einstellung

GL \_ LINE SMOOTH \_ \_ HINT-Einstellung

GL \_ POLYGON \_ SMOOTH \_ HINT-Einstellung

GL \_ GL TIPP \_ HINT-Einstellung

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL \_ LIGHTING \_ BIT
</dt> <dd>

GL \_ COLOR MATERIAL enable \_ bit

GL \_ COLOR MATERIAL FACE \_ \_ Value

Farbmaterialparameter, die die aktuelle Farbe nachverfolgen

Umgebungsszenenfarbe

GL \_ LIGHT MODEL LOCAL \_ \_ \_ VIEWER-Wert

GL \_ LIGHT MODEL TWO \_ \_ \_ SIDE-Einstellung

GL \_ LIGHTING enable bit

Bit für jedes Licht aktivieren

Umgebungs-, Diffuse- und Specular-Intensität für jedes Licht

Richtung, Position, Exponent und Abschneidewinkel für jedes Licht

Konstante, lineare und quadratische Dämpfungsfaktoren für jedes Licht

Ambient, diffuse, specular, and emissive color for each material (Umgebungsfarbe, Diffuse, Glanzfarbe und freizügige Farbe für jedes Material)

Ambient-, diffuse- und specular color-Indizes für jedes Material

Specular exponent for each material GL \_ SHADE \_ MODEL setting

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL \_ LINE \_ BIT 
</dt> <dd>

GL \_ LINE \_ SMOOTH-Flag

GL \_ LINE \_ STIPPLE enable bit

Linienstipplemuster und Wiederholungszähler

Linienstärke

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL \_ LIST \_ BIT
</dt> <dd>

GL \_ LIST \_ BASE-Einstellung

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL \_ PIXEL \_ MODE \_ BIT
</dt> <dd>

GL \_ RED \_ BIAS- und GL RED \_ \_ SCALE-Einstellungen

GL \_ GREEN \_ BIAS- und GL GREEN \_ \_ SCALE-Werte

GL \_ BLUE BIAS und GL BLUE \_ \_ \_ SCALE

GL \_ ALPHA BIAS und GL ALPHA \_ \_ \_ SCALE

GL \_ DEPTH BIAS und GL DEPTH \_ \_ \_ SCALE

GL \_ INDEX \_ OFFSET- und GL INDEX \_ \_ SHIFT-Werte

GL \_ MAP \_ COLOR- und GL MAP \_ \_ STENCIL-Flags

GL \_ ZOOM \_ X- und GL ZOOM \_ \_ Y-Faktoren

GL \_ READ \_ BUFFER-Einstellung

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL \_ POINT \_ BIT
</dt> <dd>

GL \_ POINT \_ SMOOTH-Flag

Punktgröße

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL \_ POLYGON \_ BIT
</dt> <dd>

GL \_ CULL \_ FACE enable bit

GL \_ CULL \_ FACE \_ MODE-Wert

GL \_ FRONT \_ FACE Indicator

\_GL POLYGON \_ MODE-Einstellung

GL \_ POLYGON \_ SMOOTH-Flag

GL \_ POLYGON \_ STIPPLE enable bit

GL \_ POLYGON \_ OFFSET \_ FILL-Flag

GL \_ POLYGON OFFSET LINE \_ \_ Flag

\_ \_ \_ GL-POLYGONOFFSETPUNKTflag

GL \_ POLYGON \_ OFFSET \_ FACTOR

GL \_ POLYGON \_ OFFSET \_ UNITS

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL \_ POLYGON \_ STIPPLE \_ BIT
</dt> <dd>

Polygonstipplebild

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL \_ SCISSOR \_ BIT
</dt> <dd>

GL \_ SCISSOR \_ TEST-Flag

Scissor-Box

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL \_ STENCIL \_ BUFFER \_ BIT
</dt> <dd>

GL \_ STENCIL \_ TEST enable bit

Schablonenfunktion und Verweiswert

Schablonenwertmaske

Schablonen-Aktionen zum Fehlschlagen, Übergeben und Tiefenpufferüberlauf

Stencil buffer clear value (Schablonenpuffer-Clear-Wert)

Schablonenpuffer-Schreibmaske

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL \_ TEXTURE \_ BIT
</dt> <dd>

Aktivieren von Bits für die vier Texturkoordinaten

Rahmenfarbe für jedes Texturbild

Minification-Funktion für jedes Texturbild

Vergrößerungsfunktion für jedes Texturbild

Texturkoordinaten und Umbruchmodus für jedes Texturbild

Farbe und Modus für jede Texturumgebung

Aktivieren sie die Bits GL \_ TEXTURE \_ GEN \_ *x*; *x* ist S, T, R und Q

GL \_ TEXTURE \_ GEN \_ MODE-Einstellung für S, T, R und Q

glTexGen-Ebenengleichungen für S, T, R und Q

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL \_ TRANSFORM \_ BIT
</dt> <dd>

Koeffizienten der sechs Clippingebenen

Aktivieren von Bits für die benutzerdefinierten Clippingebenen

GL \_ MATRIX \_ MODE-Wert

GL \_ NORMALIZE-Flag

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL \_ VIEWPORT \_ BIT
</dt> <dd>

Tiefenbereich (nah und fern)

Viewportursprung und -extent

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | Die Funktion wurde aufgerufen, während der Attributstapel voll war.<br/>                                                                |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glPushAttrib-Funktion** nimmt ein Argument an, eine Maske, die angibt, welche Gruppen von Zustandsvariablen im Attributstapel gespeichert werden sollen. Symbolische Konstanten werden verwendet, um Bits in der Maske festzulegen. Der mask-Parameter wird in der Regel erstellt, indem der logische **OR-Vorgang** auf mehrere dieser Konstanten angewendet wird. Sie können die spezielle Maske GL \_ ALL \_ ATTRIB \_ BITS verwenden, um alle stapelbaren Zustände zu speichern.

Die [**glPopAttrib-Funktion**](glpopattrib.md) stellt die Werte der Zustandsvariablen wieder her, die mit dem letzten **befehl glPushAttrib** gespeichert wurden. Die nicht gespeicherten werden unverändert gelassen.

Es ist ein Fehler, Attribute per Push auf einen vollständigen Stapel zu verschieben oder Attribute aus einem leeren Stapel zu verschieben. In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.

Zunächst ist der Attributstapel leer.

Nicht alle Werte für den OpenGL-Zustand können im Attributstapel gespeichert werden. Beispielsweise können Sie den Pixelpaket- und Entpackzustand, den Rendermoduszustand und den Auswahl- und Feedbackzustand nicht speichern.

Die Tiefe des Attributstapels hängt von der Implementierung ab, muss aber mindestens 16 sein.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPushAttrib** und [**glPopAttrib ab:**](glpopattrib.md)

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ ATTRIB \_ STACK \_ DEPTH

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit argument GL \_ MAX \_ ATTRIB \_ STACK \_ DEPTH

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





