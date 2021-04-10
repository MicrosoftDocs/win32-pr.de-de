---
title: glpushatpub-Funktion (GL. h)
description: Überträgt den Attribut Stapel.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- glpushatpub-Funktion OpenGL
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
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040291"
---
# <a name="glpushattrib-function"></a>glpushatpub-Funktion

Überträgt den Attribut Stapel.

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

Eine Maske, die angibt, welche Attribute gespeichert werden sollen. Die symbolischen Masken Konstanten und Ihr zugeordneter OpenGL-Zustand lauten wie folgt (in den eingerückt ten Absätzen wird aufgelistet, welche Attribute gespeichert werden):

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL- \_ Accum- \_ Puffer \_ Bit 
</dt> <dd>

Wert für Kumulations Puffer Clear

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL- \_ Farb \_ Puffer \_ Bit
</dt> <dd>

GL \_ alpha \_ Test Enable Bit

Alpha-Testfunktion und Verweis Wert

GL \_ Blend-Bit aktivieren

Mischen von Quell-und Zielfunktionen

GL \_ Dither Enable Bit

GL- \_ Zeichnen- \_ Puffereinstellung

GL \_ Logic \_ op Enable Bit

Logik-op-Funktion

Werte für den Farbmodus und den indexmodusmodus

Beschreibe-und indexmodusschreibmodus

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL \_ Aktuelles \_ Bit
</dt> <dd>

Aktuelle RGBA-Farbe

Aktueller Farbindex

Aktueller normaler Vektor

Aktuelle Texturkoordinaten

Aktuelle Raster Position GL \_ aktuelle \_ Raster \_ Position \_ gültiges Flag

RGBA-Farbe, die der aktuellen Raster Position zugeordnet ist

Der aktuellen Raster Position zugeordneter Farb Index.

Der aktuellen Raster Position zugeordnete Texturkoordinaten

GL \_ Edge-Flag-Flag \_

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL- \_ Tiefe- \_ Puffer \_ Bit
</dt> <dd>

GL- \_ tiefen \_ Test-Enable-Bit

Tiefen Puffer-Testfunktion

Tiefen Puffer-Clear-Wert

GL- \_ tiefen \_ Schreibweise für das Aktivieren des Bits

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL \_ enable \_ Bit
</dt> <dd>

GL- \_ alpha- \_ TESTFLAG

GL \_ Auto \_ Normal Flag

GL- \_ Blend-Flag

Bits für die benutzerdefinierbaren Clippingebenen aktivieren

GL- \_ Farb \_ Material

GL- \_ \_ cullface-Flag

GL- \_ tiefen \_ TESTFLAG

GL \_ Dither-Flag

GL- \_ nebelflag

GL \_ Light *i* WHERE 0 <= *i* < GL \_ Max \_ Lights

GL- \_ Beleuchtungs Flag

Glättung für GL- \_ Linie \_

GL-Zeilen Kennzeichen- \_ \_ Flag

GL \_ Color \_ Logic \_ op-Flag

GL- \_ Index \_ Logik-op- \_ Flag

GL \_ zuordnung1 \_ x, wobei x ein Kartentyp ist

GL \_ map2 \_ x, wobei x ein Kartentyp ist

GL \_ normalize-Flag

GL- \_ Punkt- \_ Smooth-Flag

GL- \_ Polygon- \_ offsesettyp \_

Füllflag für GL- \_ Polygon- \_ Offset \_

GL- \_ Polygon- \_ \_ offpunktflag

GL- \_ Polygon- \_ Smooth-Flag

GL- \_ Polygon- \_ stippflag

TESTFLAG für GL- \_ Scissor \_

GL- \_ Schablone- \_ TESTFLAG

GL \_ Texture \_ 1D-Flag

GL \_ Texture \_ 2D-Flag

Flags GL \_ Textur \_ gen \_ x, wobei x S, T, R oder Q ist

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL- \_ eval- \_ Bit
</dt> <dd>

GL \_ zuordnung1 \_ x enable Bits, wobei x ein Kartentyp ist

GL \_ map2 \_ x enable Bits, wobei x ein Kartentyp ist

1D-Raster Endpunkte und-Abteilungen

2D-Raster Endpunkte und-Abteilungen

GL \_ Auto \_ Normal Enable-Bit

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL \_ - \_ nebelbit
</dt> <dd>

GL- \_ Nebel-Aktivierungsflag

Nebelfarbe

Nebeldichte

Linearer Nebel Anfang

Lineare Nebel Ende

Nebelindex

GL \_ - \_ nebelmoduswert

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL- \_ Hinweis \_ Bit
</dt> <dd>

GL- \_ Perspektiven \_ Korrektur- \_ Hinweis Einstellung

GL- \_ Punkt- \_ Smooth Hint- \_ Einstellung

\_ \_ Smooth Hint- \_ Einstellung für GL-Linie

GL- \_ Polygon- \_ Smooth Hint- \_ Einstellung

GL- \_ Nebel- \_ Hinweis Einstellung

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL- \_ Beleuchtungs \_ Bit
</dt> <dd>

GL- \_ Farb \_ Material, Enable Bit

Wert für GL- \_ Farb \_ Material \_ Gesicht

Farb Materialparameter zum Nachverfolgen der aktuellen Farbe

Ambiente-Szene Farbe

\_Wert des \_ \_ Werts für den lokalen GL-lichtmodell \_

Das GL- \_ Light- \_ Modell mit \_ zwei \_ seitigen Einstellungen

GL- \_ Beleuchtung-Bit aktivieren

Bits für jedes Licht aktivieren

Ambient, diffuses und Glanz Intensität für jedes Licht

Richtung, Position, Exponent und Umdrehungs Winkel für jede Beleuchtung

Konstante, lineare und quadratische Dämpfungsfaktoren für jede Beleuchtung

Ambient, diffuse, Glanz und selbst leuchtendes Farbe für jedes Material

Ambient-, diffuse und Glanz Farben Indizes für jedes Material

Glanz Exponent für jede Material- \_ Schattierung- \_ Modell Einstellung

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL \_ - \_ linienbit 
</dt> <dd>

Glättung für GL- \_ Linie \_

Bereich für GL- \_ Zeilen- \_ Stippel aktivieren

Zeilen stippingmuster und Wiederholungs Counter

Linienstärke

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL- \_ Listen \_ Bit
</dt> <dd>

\_ \_ Basis Einstellung der GL-Liste

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL- \_ Pixel \_ Modus- \_ Bit
</dt> <dd>

GL. \_ Rote \_ Bias und GL-Einstellungen für die \_ Rote \_ Skala

GL \_ \_ -grüner Bias und GL- \_ grün \_ Skalierungs Werte

GL \_ Blue \_ Bias und GL \_ Blue \_ Scale

GL \_ \_ -Alpha-Bias und GL- \_ alpha \_ Skala

GL \_ \_ -Tiefe und GL- \_ tiefen \_ Skala

Werte für GL \_ \_ -Index Offset und GL- \_ Index \_ Verschiebung

GL \_ \_ -Kartenfarbe und GL- \_ Karten- \_ Stencil-Flags

\_Y Zoom \_ X-und GL \_ Zoom-Y- \_ Faktoren

GL- \_ Lese \_ Puffereinstellung

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL \_ - \_ punktbit
</dt> <dd>

GL- \_ Punkt- \_ Smooth-Flag

Punktgröße

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL- \_ Polygon- \_ Bit
</dt> <dd>

GL. \_ \_ gesichtbit aktivieren

Wert des GL- \_ cull- \_ Gesichts \_ Modus

GL- \_ Front- \_ Face-Indikator

Einstellung des GL- \_ Polygon \_ Modus

GL- \_ Polygon- \_ Smooth-Flag

GL- \_ Polygon- \_ Stippel aktivieren (Bit)

Füllflag für GL- \_ Polygon- \_ Offset \_

GL- \_ Polygon- \_ offsesettyp \_

GL- \_ Polygon- \_ \_ offpunktflag

GL- \_ Polygon- \_ Offset \_ Faktor

GL- \_ Polygon- \_ Offset \_ Einheiten

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL- \_ Polygon- \_ Stippel \_ Bit
</dt> <dd>

Polygon-Stippel Bild

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL- \_ Scheren- \_ Bit
</dt> <dd>

TESTFLAG für GL- \_ Scissor \_

Scissor-Feld

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL- \_ Schablone- \_ Puffer \_ Bit
</dt> <dd>

GL- \_ Schablone-Test-enable- \_ Bit

Schablonen Funktion und Verweis Wert

Schablone-Wert Maske

Fehler-, Pass-und Tiefe Puffer Pass Aktionen der Schablone

Unklarer Wert für Schablonen Puffer

Beschreibe-pufferfrage

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL- \_ Textur \_ Bit
</dt> <dd>

Bits für die vier Texturkoordinaten aktivieren

Rahmenfarbe für jedes Textur Bild

Minification-Funktion für jedes Textur Bild

Vergrößerungsfunktion für jedes Textur Bild

Texturkoordinaten und Umbruch Modus für jedes Textur Bild

Farbe und Modus für jede Textur Umgebung

Bits GL- \_ Textur \_ gen \_ *x* aktivieren; *x* ist S, T, R und Q

GL \_ \_ -Textur gen \_ -Modus-Einstellung für S, T, R und Q

auf gltexgen-Ebenen Gleichungen für S, T, R und Q

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL- \_ Transform- \_ Bit
</dt> <dd>

Koeffizienten der sechs Clipping-Ebenen

Bits für die benutzerdefinierbaren Clippingebenen aktivieren

Wert des GL- \_ Matrix \_ Modus

GL \_ normalize-Flag

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL- \_ \_ viewportbit
</dt> <dd>

Tiefenbereich (nah und weit)

Ursprung und Block des Viewports

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL- \_ Stapel \_ Überlauf**</dt> </dl>    | Die Funktion wurde aufgerufen, während der Attribut Stapel voll war.<br/>                                                                |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " **glpushatpub** " erfordert ein Argument, eine Maske, die angibt, welche Gruppen von Zustandsvariablen im Attribut Stapel gespeichert werden sollen. Symbolische Konstanten werden verwendet, um Bits in der Maske festzulegen. Der mask-Parameter wird in der Regel erstellt, indem der logische **or** -Vorgang auf mehrere dieser Konstanten angewendet wird. Sie können den Wert "Special Mask GL \_ All \_ atzb" verwenden \_ , um alle Stackable-Zustände zu speichern.

Die Funktion " [**glpopatpub**](glpopattrib.md) " stellt die Werte der Zustandsvariablen wieder her, die mit dem letzten Befehl " **glpushatpub** " gespeichert wurden. Die nicht gespeicherten Änderungen bleiben unverändert.

Es ist ein Fehler, Attribute auf einen vollständigen Stapel zu übersetzen oder Attribute aus einem leeren Stapel zu Pop. In beiden Fällen wird das Fehlerflag festgelegt, und es wird keine andere Änderung am OpenGL-Zustand vorgenommen.

Der Attribut Stapel ist zunächst leer.

Nicht alle Werte für den OpenGL-Zustand können im Attribut Stapel gespeichert werden. Sie können z. b. das Pixel Paket nicht speichern und den Zustand des rendermoduszustands sowie den Zustand "Status" und "Feedback" auswählen.

Die Tiefe des Attribut Stapels hängt von der Implementierung ab, muss jedoch mindestens 16 sein.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glpushatpub** und [**glpopatpub**](glpopattrib.md)ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ \_ Stapel \_ Tiefe des Argument-GL

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ maximalen \_ attrb- \_ Stapel \_ Tiefe des Arguments

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glgetclipplane**](glgetclipplane.md)
</dt> <dt>

[**glgeterror**](glgeterror.md)
</dt> <dt>

[**glgetlight**](glgetlight.md)
</dt> <dt>

[**glgetmap**](glgetmap.md)
</dt> <dt>

[**glgetmaterial**](glgetmaterial.md)
</dt> <dt>

[**glgetpixelmap**](glgetpixelmap.md)
</dt> <dt>

[**glgetpolygonstippel**](glgetpolygonstipple.md)
</dt> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**glgettex-v**](glgettexenv.md)
</dt> <dt>

[**glgettexgen**](glgettexgen.md)
</dt> <dt>

[**glgetteximage**](glgetteximage.md)
</dt> <dt>

[**glgettexlevelparameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> </dl>

 

 





