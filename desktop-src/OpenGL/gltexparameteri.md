---
title: gltexparameteri-Funktion (GL. h)
description: Legt Textur Parameter fest. | gltexparameteri-Funktion (GL. h)
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
keywords:
- gltexparameteri-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexParameteri
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207ac902047c5a2b6a5266d08e71f8e47f7ccb97
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352719"
---
# <a name="gltexparameteri-function"></a>gltexparameteri-Funktion

Legt Textur Parameter fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexParameteri(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Ziel Textur, die entweder GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D sein muss.

</dd> <dt>

*pName* 
</dt> <dd>

Der symbolische Name eines einwertigen Textur Parameters. Die folgenden Symbole werden in " *PName*" akzeptiert.



| Wert                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**GL- \_ Textur- \_ Min- \_ Filter**</dt> </dl> | Die Textur miniierungsfunktion wird immer dann verwendet, wenn das zu Textende Pixel einem Bereich zugeordnet wird, der größer als ein Textur Element ist. Es gibt sechs definierte minisierungs Funktionen. Zwei von Ihnen verwenden das nächstgelegene oder das nächste vier Textur Element, um den Textur Wert zu berechnen. Die anderen vier verwenden Mipmaps. <br/> Eine MipMap ist eine geordnete Gruppe von Arrays, die das gleiche Bild bei progressiv niedrigeren Auflösungen darstellen. Wenn die Textur Dimensionen 2nx2<sup>m</sup> aufweist, sind Max (n, m) + 1 Mipmaps vorhanden. Die erste MipMap ist die ursprüngliche Textur mit den Dimensionen 2nx2<sup>m</sup>. Jede nachfolgende MipMap weist die Dimensionen 2<sup>k</sup>1X2<sup>l</sup>1 auf, wobei 2<sup>k</sup>x2<sup>l</sup> die Dimensionen der vorherigen MipMap sind, bis entweder k = 0 oder l = 0. An diesem Punkt verfügen nachfolgende Mipmaps über die Dimension 1X2<sup>l</sup>1 oder 2<sup>k</sup>1x1 bis zur endgültigen MipMap mit der Dimension 1x1. Mipmaps werden mithilfe von [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md) mit dem Detail Argument definiert, das die Reihenfolge der Mipmaps angibt. Ebene 0 ist die ursprüngliche Textur. der Höchstwert für die Fett formatierte Ebene (n, m) ist die abschließende 1x1-MipMap.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**GL- \_ Textur- \_ mag- \_ Filter**</dt> </dl> | Die Textur Vergrößerungsfunktion wird verwendet, wenn das zu strukturierte Pixel einem Bereich entspricht, der kleiner oder gleich einem Textur Element ist. Der Wert für die Textur Vergrößerung wird entweder auf "GL \_ Next" oder "GL linear" festgelegt \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL- \_ Textur Umbruch \_ \_ S**</dt> </dl>             | Legt den Wrap-Parameter für Texturkoordinaten s auf die GL- \_ Klammer oder die GL- \_ Wiederholung fest. \_Die GL-Klammer bewirkt, dass die Koordinaten an den Bereich \[ 0, 1 gebunden werden, \] und ist nützlich, um das Umwickeln von Artefakten beim Mapping eines einzelnen Bilds zu einem Objekt zu verhindern. GL \_ Repeat bewirkt, dass der ganzzahlige Teil der s-Koordinate ignoriert wird. OpenGL verwendet nur die Bruchteile und erstellt dadurch ein sich wiederholendes Muster. Auf Rahmen Textur Elemente wird nur zugegriffen, wenn Wrapping auf GL-Klammer festgelegt ist \_ . Zunächst ist GL \_ Texture \_ Wrap \_ S auf GL Repeat festgelegt \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL- \_ Textur Umbruch \_ \_ T**</dt> </dl>             | Legt den Wrap-Parameter für die Texturkoordinaten t entweder auf die GL- \_ Klammer oder die GL- \_ Wiederholung fest. Weitere Informationen finden Sie unter GL \_ Texture \_ Wrap \_ S. Anfänglich \_ ist GL Texture \_ Wrap \_ T auf GL Repeat festgelegt \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert von " *PName*".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ . Ungültige \_** Aufzählung.</dt> </dl>     | *target* oder *PName* war keiner der zulässigen Werte oder, wenn *param* einen definierten Konstanten Wert aufweisen sollte (basierend auf dem Wert von *PName*) und nicht.<br/> |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                            |



## <a name="remarks"></a>Bemerkungen

Die Textur Zuordnung ist eine Technik, die ein Bild auf die Oberfläche eines Objekts anwendet, als ob es sich bei dem Bild um eine Debug-oder Cellophane-Verkleinerung handelt. Das Bild wird im Textur Raum mit einem-Koordinatensystem (*s*, *t*) erstellt. Eine Textur ist ein ein-oder zweidimensionales Bild und eine Reihe von Parametern, die bestimmen, wie Beispiele vom Bild abgeleitet werden.

Die Funktion " **gltexparameter** " weist den Wert oder die Werte in den Parametern dem als "pname" angegebenen Textur Parameter zu. Der Zielparameter definiert die Ziel Textur, entweder GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D.

Wenn bei der Minimierung mehr Textur Elemente als Stichprobe genommen werden, werden weniger Aliasing-Artefakte offensichtlich. Obwohl die \_ Funktionen von "adnext" und "GL \_ linear Minimierung" schneller als die anderen vier sind, werden nur ein oder vier Textur Elemente als Stichprobe für den Textur Wert des gerenderten Pixels festgelegt, und es können Muster oder unregelmäßige Übergänge erzeugt werden. Der Standardwert des GL- \_ Textur \_ Min- \_ Filters ist GL \_ nächstgelegene \_ MipMap \_ linear.

Angenommen, die Texturierung ist aktiviert (durch Aufrufen von [**glEnable**](glenable.md) mit dem Argument GL \_ Texture \_ 1D oder GL \_ Texture \_ 2D), und der GL- \_ Textur \_ Min- \_ Filter wird auf eine der Funktionen festgelegt, für die eine MipMap erforderlich ist. Wenn entweder die Dimensionen der derzeit definierten Textur Bilder (mit vorherigen Aufrufen von [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md)) nicht der richtigen Reihenfolge für Mipmaps entsprechen oder weniger Textur Bilder definiert sind, als erforderlich sind, oder wenn der Satz von Textur Bildern eine abweichende Anzahl von texturkomponenten hat, ist dies so, als ob die Textur Zuordnung deaktiviert wäre. Die lineare Filterung greift auf die vier nächsten Textur Elemente nur in 2D-Texturen zu. Bei 1-D-Texturen greift die lineare Filterung auf die beiden nächsten Textur Elemente zu. Die folgende Funktion Ruft Informationen im Zusammenhang mit **gltexparameterf**, **gltexparameteri**, **gltexparameterfv** und **gltexparameteriv** ab:

[**glgettexparameter**](glgettexparameter.md)

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glgettexparameter**](glgettexparameter.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glpriorizetexturen**](glprioritizetextures.md)
</dt> <dt>

[gltexd](gltexenv-functions.md)
</dt> <dt>

[gltexgen](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





