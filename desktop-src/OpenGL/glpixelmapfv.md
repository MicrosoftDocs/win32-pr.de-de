---
title: glPixelMapfv-Funktion (Gl.h)
description: Die glPixelMapfv-Funktion richtet Pixelübertragungszuordnungen ein.
ms.assetid: 13403243-1ec4-4b1d-a9da-9a6693b6f9b8
keywords:
- glPixelMapfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e447e471f1a37f4d0c8c6bd8fb3ce548bb5657e49afafa01e785b0870ebdd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938355"
---
# <a name="glpixelmapfv-function"></a>glPixelMapfv-Funktion

Die **glPixelMapfv-Funktion** richtet Pixelübertragungszuordnungen ein.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPixelMapfv(
         GLenum  map,
         GLsizei mapsize,
   const GLfloat *values
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*map* 
</dt> <dd>

Ein symbolischer Zuordnungsname. Die zehn Zuordnungen sind wie folgt.



| Wert                                                                                                                                                                               | Bedeutung                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ I**</dt> </dl> | Karten Farbindizes in Farbindizes ein.<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ S \_ TO \_ S**</dt> </dl> | Karten Schablonenindizes zu Schablonenindizes.<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ R**</dt> </dl> | Karten Farbindizes an rote Komponenten an.<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ G**</dt> </dl> | Karten Farbindizes zu grünen Komponenten an.<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ B**</dt> </dl> | Karten Farbindizes zu blauen Komponenten.<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ I \_ TO \_ A**</dt> </dl> | Karten Farbindizes für Alphakomponenten an.<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ R \_ TO \_ R**</dt> </dl> | Karten roter Komponenten zu roten Komponenten.<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ G \_ TO \_ G**</dt> </dl> | Karten grüne Komponenten zu grünen Komponenten.<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ B \_ TO \_ B**</dt> </dl> | Karten blauer Komponenten zu blauen Komponenten.<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**GL \_ PIXEL \_ MAP \_ A \_ TO \_ A**</dt> </dl> | Karten Alphakomponenten zu Alphakomponenten.<br/> |



 

</dd> <dt>

*mapsize* 
</dt> <dd>

Die Größe der zu definierenden Karte.

</dd> <dt>

*Werte* 
</dt> <dd>

Ein Array von *Zuordnungswerten.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *map* war kein akzeptierter Wert.<br/>                                                                                                                                                                                |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *mapsize* war negativ oder größer als GL \_ PIXEL \_ MAP \_ TABLE. <br/>                                                                                                                                                   |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl>     | *Map* war GL \_ PIXEL MAP I TO \_ \_ \_ \_ I, GL PIXEL MAP \_ S TO \_ \_ \_ \_ S, GL PIXEL MAP I \_ TO \_ \_ \_ \_ R, GL PIXEL MAP I \_ TO \_ \_ \_ \_ G, GL PIXEL MAP \_ I TO B oder GL PIXEL MAP I TO \_ A \_ und \_ \_ \_ \_ \_ \_ \_ *mapsize* war keine Potenz von zwei. <br/> |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen. <br/>                                                                                     |



## <a name="remarks"></a>Hinweise

Die **glPixelMap-Funktion** richtet Übersetzungstabellen ein oder *ordnet* zu, die von [**glCopyPixels,**](glcopypixels.md) [**glCopyTexImage1D,**](glcopyteximage1d.md) [**glCopyTexImage2D,**](glcopyteximage2d.md) [**glCopyTexSubImage1D,**](glcopytexsubimage1d.md) [**glCopyTexSubImage2D,**](glcopytexsubimage2d.md) [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels,**](glreadpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)und [**glTexSubImage2D**](gltexsubimage2d.md)verwendet werden. Die Verwendung dieser Zuordnungen wird vollständig im Thema [**glPixelTransfer**](glpixeltransfer.md) und teilweise in den Themen für die Pixel- und Texturbildbefehle beschrieben. In diesem Thema wird nur die Spezifikation der Zuordnungen beschrieben.

Der *Map-Parameter* ist ein symbolischer Kartenname, der eine von zehn festzulegende Zuordnungen angibt. Der *Mapsize-Parameter* gibt die Anzahl von Einträgen in der Karte an, und *Werte* sind ein Zeiger auf ein Array von *Kartenwerten* für Kartenzuordnungen.

Die Einträge in einer Zuordnung können als Gleitkommazahlen mit einfacher Genauigkeit, kurze ganze Zahlen ohne Vorzeichen oder ganze Zahlen ohne Vorzeichen angegeben werden. Karten, die Farbkomponentenwerte speichern (alle außer GL \_ PIXEL MAP I TO I und GL PIXEL MAP \_ S TO \_ \_ \_ \_ \_ \_ \_ \_ S), behalten ihre Werte im Gleitkommaformat mit nicht angegebenen Mantisse- und Exponentengrößen bei. Gleitkommawerte, die von [**glPixelMapfv**](glpixelmap.md) angegeben werden, werden direkt in das interne Gleitkommaformat dieser Zuordnungen konvertiert und dann an den Bereich \[ 0,1 \] gebunden. Durch **glPixelMapusv** und **glPixelMapuiv** angegebene ganzzahlige Werte ohne Vorzeichen werden linear konvertiert, sodass die größte darstellbare ganze Zahl 1,0 und null 0,0 zugeordnet wird.

Karten, die Indizes, GL \_ PIXEL \_ MAP I TO I und GL PIXEL MAP S \_ TO \_ \_ \_ \_ \_ \_ \_ S, speichern, behalten ihre Werte im Festkommaformat mit einer nicht angegebenen Anzahl von Bits rechts vom Binärpunkt bei. Gleitkommawerte, die von [**glPixelMapfv**](glpixelmap.md) angegeben werden, werden direkt in das interne Festkommaformat dieser Zuordnungen konvertiert. Ganzzahlige Werte ohne Vorzeichen, die von **glPixelMapusv** und **glPixelMapuiv** angegeben werden, geben ganzzahlige Werte an, wobei alle Nullen rechts neben dem Binärpunkt angezeigt werden.

Die folgende Tabelle zeigt die Anfangsgrößen und -werte für jede der Zuordnungen. Karten, die entweder durch Farb- oder Schablonenindizes indiziert werden, müssen für einige *n* *zuordnungen* = 2 ^ *n* aufweisen, oder Ergebnisse sind nicht definiert. Die maximal zulässige Größe für jede Zuordnung hängt von der Implementierung ab und kann durch Aufrufen von **glGet** mit dem Argument GL MAX PIXEL MAP TABLE bestimmt \_ \_ \_ \_ werden. Der einzelne Höchstwert gilt für alle Zuordnungen und ist mindestens 32.



| Zuordnung                      | Suchindex  | Suchwert  | Anfangsgröße | Anfangswert |
|--------------------------|---------------|---------------|--------------|---------------|
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ I | Farbindex   | Farbindex   | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ S \_ TO \_ S | Schablonenindex | Schablonenindex | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ R | Farbindex   | R             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ G | Farbindex   | G             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ B | Farbindex   | B             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ I \_ TO \_ A | Farbindex   | Ein             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ R \_ TO \_ R | R             | R             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ G \_ TO \_ G | G             | G             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ B \_ TO \_ B | B             | B             | 1            | 0,0           |
| GL \_ PIXEL \_ MAP \_ A \_ TO \_ A | Ein             | Ein             | 1            | 0,0           |



 

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPixelMap** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ PIXEL MAP I TO I \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP S TO S \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP I TO R \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP I TO G \_ \_ \_ \_ \_ SIZE

**glGet** mit Argument GL \_ PIXEL MAP I TO B \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP I TO A \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP R TO R \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP G TO G \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP B TO B \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ PIXEL MAP A TO A \_ \_ \_ \_ \_ SIZE

**glGet** mit argument GL \_ MAX PIXEL MAP \_ \_ \_ TABLE

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





