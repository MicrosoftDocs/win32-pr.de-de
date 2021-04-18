---
title: glpixelmapusv-Funktion (GL. h)
description: Die glpixelmapusv-Funktion richtet Pixel Übertragungs Zuordnungen ein.
ms.assetid: c542a1be-8fb0-4269-afc0-459182c89534
keywords:
- glpixelmapusv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dd4adc50af4a4168d14ac2e39d465ace360ccbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338533"
---
# <a name="glpixelmapusv-function"></a>glpixelmapusv-Funktion

Die **glpixelmapusv** -Funktion richtet Pixel Übertragungs Zuordnungen ein.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPixelMapusv(
         GLenum   map,
         GLsizei  mapsize,
   const GLushort *values
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*map* 
</dt> <dd>

Ein symbolischer Zuordnungs Name. Die zehn Zuordnungen lauten wie folgt.



| Wert                                                                                                                                                                               | Bedeutung                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**GL \_ Pixel \_ map \_ i \_ to \_ i**</dt> </dl> | Ordnet Farbindizes Farbindizes zu.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**GL- \_ Pixel \_ map \_ s \_ zu \_ s**</dt> </dl> | Ordnet Schablonen Indizes zu Schablonen Indizes zu.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**GL \_ Pixel \_ map \_ I \_ to \_ R**</dt> </dl> | Ordnet Farbindizes zu roten Komponenten zu.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**GL \_ Pixel \_ map \_ I \_ to \_ G**</dt> </dl> | Ordnet Farbindizes zu grünen Komponenten zu.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**GL \_ Pixel \_ map \_ I \_ to \_ B**</dt> </dl> | Ordnet Farbindizes zu blauen Komponenten zu.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**GL \_ Pixel \_ map \_ I \_ to \_ A**</dt> </dl> | Ordnet den Alpha Komponenten Farbindizes zu.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**GL \_ Pixel \_ map \_ r \_ to \_ r**</dt> </dl> | Ordnet rote Komponenten roten Komponenten zu.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**GL \_ Pixel \_ map \_ g \_ bis \_ g**</dt> </dl> | Ordnet die grünen Komponenten grünen Komponenten zu.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**GL \_ Pixel \_ map \_ b \_ zu \_ b**</dt> </dl> | Ordnet blaue Komponenten blauen Komponenten zu.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**GL- \_ Pixel zuordnen \_ \_ eines \_ zu \_ einem**</dt> </dl> | Ordnet Alpha Komponenten Alpha Komponenten zu.<br/> |



 

</dd> <dt>

*mapsize* 
</dt> <dd>

Die Größe der Karte, die definiert wird.

</dd> <dt>

*Werte* 
</dt> <dd>

Ein Array von *mapsize* -Werten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | *map* war kein akzeptierter Wert.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *mapsize* war negativ oder größer als die GL- \_ Pixel \_ map- \_ Tabelle. <br/>                                                                                                                                                   |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl>     | *map* war GL \_ Pixel \_ map \_ i \_ to \_ i, GL \_ Pixel \_ map \_ s \_ to \_ s, GL \_ Pixel \_ map \_ i \_ to \_ R, GL \_ Pixel \_ map \_ i \_ to \_ G, GL \_ Pixel \_ map \_ i \_ to \_ B oder GL-Pixel Map i to \_ \_ a, \_ \_ \_ und *mapsize* war keine Potenz von zwei. <br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen. <br/>                                                                                     |



## <a name="remarks"></a>Bemerkungen

Die **glpixelmap** -Funktion richtet Übersetzungstabellen oder *Maps* ein, die von [**glcopypixel**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**gldrawpixels**](gldrawpixels.md), [**gllepixel**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)und [**glTexSubImage2D**](gltexsubimage2d.md)verwendet werden. Die Verwendung dieser Zuordnungen wird vollständig im Thema [**glpixeltransfer**](glpixeltransfer.md) beschrieben und teilweise in den Themen für die Befehle Pixel und Textur Bild beschrieben. In diesem Thema wird nur die Spezifikation der Maps beschrieben.

Der *map* -Parameter ist ein symbolischer Kartenname, der eine von zehn Zuordnungen angibt, die festgelegt werden sollen. Der *mapsize* -Parameter gibt die Anzahl der Einträge in der Zuordnung an, und *Werte* sind ein Zeiger auf ein Array von *mapsize* -Kartenwerten.

Die Einträge in einer Zuordnung können als Gleit Komma Zahlen mit einfacher Genauigkeit, kurze Ganzzahlen ohne Vorzeichen oder lange ganze Zahlen ohne Vorzeichen angegeben werden. Zuordnungen, die Farb Komponentenwerte speichern (alle außer GL \_ Pixel \_ map \_ i \_ \_ und GL \_ Pixel \_ map \_ s \_ to \_ s) behalten ihre Werte im Gleit Komma Format bei, wobei nicht angegebene Mantisse und Exponent-Größen nicht angegeben werden. Gleit Komma Werte, die von [**glpixelmapfv**](glpixelmap.md) angegeben werden, werden direkt in das interne Gleit Komma Format dieser Zuordnungen konvertiert und dann an den Bereich \[ 0, 1 gebunden \] . Ganzzahlige Werte ohne Vorzeichen, die von **glpixelmapusv** und **glpixelmapuiv** angegeben werden, werden linear konvertiert, sodass die größte darstellbare Ganzzahl 1,0 und 0 (null) 0,0 zugeordnet wird.

Zuordnungen zum Speichern von Indizes, GL \_ Pixel \_ map \_ i \_ \_ und GL \_ Pixel \_ map \_ s \_ zu \_ s, beibehalten ihrer Werte im fest Komma Format, wobei eine nicht angegebene Anzahl von Bits auf der rechten Seite des binären Punkts angezeigt wird. Gleit Komma Werte, die von [**glpixelmapfv**](glpixelmap.md) angegeben werden, werden direkt in das interne fest Komma Format dieser Zuordnungen konvertiert. Ganzzahlige Werte ohne Vorzeichen, die von **glpixelmapusv** und **glpixelmapuiv** angegeben werden, geben ganzzahlige Werte mit allen Nullen auf der rechten Seite des binären Punkts an.

In der folgenden Tabelle werden die anfänglichen Größen und Werte für jede der Zuordnungen angezeigt. Zuordnungen, die von Farb-oder Schablonen Indizes indiziert werden, müssen *mapsize* = 2 ^ *n* für einige *n* oder Ergebnisse sind nicht definiert. Die maximal zulässige Größe für jede Zuordnung hängt von der Implementierung ab und kann durch Aufrufen von **glget** mit dem Argument GL \_ Max \_ Pixel \_ map \_ Table festgelegt werden. Das einzige Maximum gilt für alle Zuordnungen und ist mindestens 32.



| Zuordnung                      | Suchindex  | Such Wert  | Anfangsgröße | Anfangswert |
|--------------------------|---------------|---------------|--------------|---------------|
| GL \_ Pixel \_ map \_ i \_ to \_ i | Farbindex   | Farbindex   | 1            | 0,0           |
| GL- \_ Pixel \_ map \_ s \_ zu \_ s | Schablone-Index | Schablone-Index | 1            | 0,0           |
| GL \_ Pixel \_ map \_ I \_ to \_ R | Farbindex   | R             | 1            | 0,0           |
| GL \_ Pixel \_ map \_ I \_ to \_ G | Farbindex   | G             | 1            | 0,0           |
| GL \_ Pixel \_ map \_ I \_ to \_ B | Farbindex   | B             | 1            | 0,0           |
| GL \_ Pixel \_ map \_ I \_ to \_ A | Farbindex   | A             | 1            | 0,0           |
| GL \_ Pixel \_ map \_ r \_ to \_ r | R             | R             | 1            | 0,0           |
| GL \_ Pixel \_ map \_ g \_ bis \_ g | G             | G             | 1            | 0,0           |
| GL \_ Pixel \_ map \_ b \_ zu \_ b | B             | B             | 1            | 0,0           |
| GL- \_ Pixel zuordnen \_ \_ eines \_ zu \_ einem | Ein             | A             | 1            | 0,0           |



 

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glpixelmap** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Pixel \_ map \_ i \_ to \_ i \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ s \_ to \_ s \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ R \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ G \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ B \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ I \_ to \_ A \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ r \_ to \_ r \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ g \_ bis \_ g \_ size

**glget** mit Argument GL \_ Pixel \_ map \_ b \_ bis \_ b \_ size

**glget** mit dem Argument GL \_ Pixel \_ map \_ a \_ to \_ a \_ size

**glget** mit dem Argument GL \_ Max \_ Pixel \_ map \_ Table

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

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





