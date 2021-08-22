---
title: glTexParameterfv-Funktion (Gl.h)
description: Legt Texturparameter fest. | glTexParameterfv-Funktion (Gl.h)
ms.assetid: 29aa2823-5c73-48f1-891f-018dd7a93323
keywords:
- glTexParameterfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexParameterfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433a886ac7094a28e7c936eb02dd55743bf1abe6a94b128fb98b42bb1bad8335
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490060"
---
# <a name="gltexparameterfv-function"></a>glTexParameterfv-Funktion

Legt Texturparameter fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glTexParameterfv(
         GLenum  target,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Die Zieltextur, die entweder GL \_ TEXTURE \_ 1D oder GL \_ TEXTURE \_ 2D sein muss.

</dd> <dt>

*pname* 
</dt> <dd>

Der symbolische Name eines einwertigen Texturparameters. Die folgenden Symbole werden in *pname* akzeptiert.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**GL \_ TEXTURE \_ MIN \_ FILTER**</dt> </dl>       | Die Texturverkleinerungsfunktion wird immer dann verwendet, wenn das zu texturierende Pixel einem Bereich zugeordnet wird, der größer als ein Texturelement ist. Es gibt sechs definierte Vergrößerungsfunktionen. Zwei von ihnen verwenden das nächste oder die nächsten vier Texturelemente, um den Texturwert zu berechnen. Die anderen vier verwenden Mipmaps. <br/> Eine Mipmap ist eine geordnete Gruppe von Arrays, die das gleiche Bild mit progressiv niedrigeren Auflösungen darstellen. Wenn die Textur die Abmessungen 2nx2<sup>m</sup> aufweist, gibt es max(n, m) + 1 mipmaps. Die erste Mipmap ist die ursprüngliche Textur mit den Abmessungen 2nx2<sup>m</sup>. Jede nachfolgende Mipmap hat die Abmessungen 2<sup>k</sup>1x2<sup>l</sup>1, wobei 2<sup>k</sup>x2<sup>l</sup> die Dimensionen der vorherigen Mipmap sind, bis entweder k = 0 oder l = 0 ist. An diesem Punkt haben nachfolgende Mipmaps die Dimension 1x2<sup>l</sup>1 oder 2<sup>k</sup>1x1 bis zur endgültigen Mipmap, die die Dimension 1x1 aufweist. Mipmaps werden [**mithilfe von glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md) mit dem Detailebenenargument definiert, das die Reihenfolge der Mipmaps angibt. Ebene 0 ist die ursprüngliche Textur. level bold max(n, m) ist die endgültige 1x1-Mipmap.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**GL \_ TEXTURE \_ MAG \_ FILTER**</dt> </dl>       | Die Texturvergrößerungsfunktion wird verwendet, wenn das texturierte Pixel einem Bereich zugeordnet wird, der kleiner oder gleich einem Texturelement ist. Die Texturvergrößerungsfunktion wird entweder auf GL \_ NEAREST oder GL \_ LINEAR festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>                   | Legt den Wrap-Parameter für Texturkoordinaten entweder auf GL \_ WRAP oder GL REPEAT \_ fest. GL WRAP bewirkt, dass die Koordinaten von an \_ den Bereich 0,1 angeklammern werden, und ist nützlich, um das \[ \] Umschließen von Artefakten zu verhindern, wenn ein einzelnes Bild einem Objekt zugeordnet wird. GL \_ REPEAT bewirkt, dass der ganzzahlige Teil der -Koordinate ignoriert wird. OpenGL verwendet nur den Bruchteil, wodurch ein sich wiederholendes Muster erstellt wird. Auf Rahmentexturelemente wird nur zugegriffen, wenn wrapping auf GL WRAP festgelegt \_ ist. Zunächst wird GL \_ TEXTURE WRAP S auf GL REPEAT \_ \_ \_ festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>                   | Legt den Wrap-Parameter für die Texturkoordinate t entweder auf GL \_ WRAP oder GL REPEAT \_ fest. Weitere Informationen finden Sie in der Diskussion unter GL \_ TEXTURE \_ WRAP \_ S. Zunächst wird GL \_ TEXTURE WRAP T auf GL REPEAT \_ \_ \_ festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**GL \_ TEXTURE \_ BORDER \_ COLOR**</dt> </dl> | Legt eine Rahmenfarbe fest. Der *parameter-Parameter* enthält vier Werte, die die RGBA-Farbe des Texturrahmens bilden. Ganzzahlige Farbkomponenten werden linear interpretiert, sodass die positivste ganze Zahl 1,0 und die negativste ganze Zahl 1,0 zugeordnet wird. Die Werte werden an den Bereich \[ 0,1 klammern, \] wenn sie angegeben werden. Anfänglich ist die Rahmenfarbe (0, 0, 0, 0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**GL \_ TEXTURE \_ PRIORITY**</dt> </dl>              | Gibt die Texturpriorität der aktuell gebundenen Textur an. Zulässige Werte liegen im Bereich \[ von 0, \] 1. Weitere Informationen finden Sie unter [**glPrioritizeTextures**](glprioritizetextures.md) und [**glBindTexture.**](glbindtexture.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*params* 
</dt> <dd>

Ein Zeiger auf ein Array, in dem der Wert oder die Werte von pname gespeichert werden. Der parameter-Parameter stellt eine Funktion zum Verminen der Textur wie eine der folgenden zur Verfügung.



| Wert                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ NEAREST**</dt> </dl>                                             | Gibt den Wert des Texturelements zurück, das dem Mittelpunkt des texturierten Pixels am nächsten ist (in der Entfernung von Centre). <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**GL \_ LINEAR**</dt> </dl>                                                   | Gibt den gewichteten Durchschnitt der vier Texturelemente zurück, die der Mitte des zu texturenden Pixels am nächsten liegen. Dazu können Rahmentexturelemente gehören, abhängig von den Werten von GL \_ TEXTURE \_ WRAP \_ S, GL TEXTURE WRAP \_ T und der \_ \_ genauen Zuordnung. GL \_ NEAREST ist im Allgemeinen schneller als GL \_ LINEAR, kann jedoch texturierte Bilder mit schärferen Kanten erzeugen, da der Übergang zwischen Texturelementen nicht so reibungslos verläuft. Der Standardwert von GL \_ TEXTURE MAG FILTER ist GL \_ \_ \_ LINEAR.<br/> |
| <span id="GL_NEAREST_MIPMAP_NEAREST"></span><span id="gl_nearest_mipmap_nearest"></span><dl> <dt>**GL \_ NEAREST \_ MIPMAP \_ NEAREST**</dt> </dl> | Wählt die Mipmap aus, die der Größe des texturierten Pixels am besten entspricht, und verwendet das GL \_ NEAREST-Kriterium (das Texturelement, das der Mitte des Pixels am nächsten ist), um einen Texturwert zu erzeugen. <br/>                                                                                                                                                                                                                                                                                              |
| <span id="GL_LINEAR_MIPMAP_NEAREST"></span><span id="gl_linear_mipmap_nearest"></span><dl> <dt>**GL \_ LINEAR \_ MIPMAP \_ NEAREST**</dt> </dl>    | Wählt das Mipmap aus, das der Größe des texturierten Pixels am besten entspricht, und verwendet das GL \_ LINEAR-Kriterium (einen gewichteten Durchschnitt der vier Texturelemente, die der Mitte des Pixels am nächsten liegen), um einen Texturwert zu erzeugen. <br/>                                                                                                                                                                                                                                                          |
| <span id="GL_NEAREST_MIPMAP_LINEAR"></span><span id="gl_nearest_mipmap_linear"></span><dl> <dt>**GL \_ NEAREST \_ MIPMAP \_ LINEAR**</dt> </dl>    | Wählt die beiden Mipmaps aus, die der Größe des texturierten Pixels am nächsten sind, und verwendet das GL \_ NEAREST-Kriterium (das Texturelement, das der Mitte des Pixels am nächsten ist), um einen Texturwert aus jeder Mipmap zu erzeugen. Der endgültige Texturwert ist ein gewichteter Durchschnitt dieser beiden Werte. <br/>                                                                                                                                                                                                       |
| <span id="GL_LINEAR_MIPMAP_LINEAR"></span><span id="gl_linear_mipmap_linear"></span><dl> <dt>**GL \_ LINEAR \_ MIPMAP \_ LINEAR**</dt> </dl>       | Wählt die beiden Mipmaps aus, die am besten mit der Größe des texturierten Pixels übereinstimmen, und verwendet das GL \_ LINEAR-Kriterium (einen gewichteten Durchschnitt der vier Texturelemente, die der Mitte des Pixels am nächsten liegen), um einen Texturwert aus jeder Mipmap zu erzeugen. Der endgültige Texturwert ist ein gewichteter Durchschnitt dieser beiden Werte.<br/>                                                                                                                                                                    |



 

Der *Parameter params* stellt eine Funktion zum Vergrößern der Textur als eine der folgenden Funktionen zur Verfügung.



| Wert                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ NEAREST**</dt> </dl> | Gibt den Wert des Texturelements zurück, das dem Mittelpunkt des texturierten Pixels am nächsten ist (in der Entfernung von Centre). <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**GL \_ LINEAR**</dt> </dl>       | Gibt den gewichteten Durchschnitt der vier Texturelemente zurück, die der Mitte des zu texturenden Pixels am nächsten liegen. Dazu können Rahmentexturelemente gehören, abhängig von den Werten von GL \_ TEXTURE \_ WRAP \_ S, GL TEXTURE WRAP \_ T und der \_ \_ genauen Zuordnung. GL \_ NEAREST ist im Allgemeinen schneller als GL \_ LINEAR, kann jedoch texturierte Bilder mit schärferen Kanten erzeugen, da der Übergang zwischen Texturelementen nicht so reibungslos verläuft. Der Standardwert von GL \_ TEXTURE MAG FILTER ist GL \_ \_ \_ LINEAR.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ UNGÜLTIGE \_ ENUMERATION**</dt> </dl>     | *target* oder *pname* war keiner der akzeptierten definierten Werte, oder wenn *param* über einen definierten konstanten Wert verfügen sollte (basierend auf dem Wert von *pname*) und nicht.<br/> |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/>                                            |



## <a name="remarks"></a>Hinweise

Texturzuordnung ist eine Technik, bei der ein Bild auf die Oberfläche eines Objekts angewendet wird, als wäre das Bild ein decal oder cellophane shrink-wrap. Das Bild wird im Texturraum mit einem Koordinatensystem (*s*, *t*) erstellt. Eine Textur ist ein ein- oder zweidimensionales Bild und eine Reihe von Parametern, die bestimmen, wie Stichproben vom Bild abgeleitet werden.

Die **glTexParameter-Funktion** weist den Wert oder die Werte in Parametern dem Texturparameter zu, der als pname angegeben ist. Der Zielparameter definiert die Zieltextur, entweder GL \_ TEXTURE \_ 1D oder GL \_ TEXTURE \_ 2D.

Wenn mehr Texturelemente im Minification-Prozess entnommen werden, sind weniger Aliasartefakte erkennbar. Die \_ Gl NEAREST- und GL \_ LINEAR- Minification-Funktionen können zwar schneller sein als die anderen vier, aber sie stichprobenieren nur ein oder vier Texturelemente, um den Texturwert des zu renderenden Pixels zu bestimmen, und können Mintermuster oder unregelmäßige Übergänge erzeugen. Der Standardwert von GL \_ TEXTURE MIN FILTER ist GL \_ \_ \_ NEAREST \_ MIPMAP \_ LINEAR.

Angenommen, die Texturierung ist aktiviert (durch Aufrufen von [**glEnable**](glenable.md) mit dem Argument GL \_ TEXTURE \_ 1D oder GL \_ TEXTURE \_ 2D) und GL \_ TEXTURE MIN FILTER ist auf eine der Funktionen \_ \_ festgelegt, die eine Mipmap erfordern. Wenn die Dimensionen der aktuell definierten Texturbilder (mit vorherigen Aufrufen von [**glTexImage1D**](glteximage1d.md) oder [**glTexImage2D)**](glteximage2d.md)nicht der richtigen Sequenz für Mipmaps folgen oder weniger Texturbilder definiert sind, als benötigt werden, oder der Satz von Texturbildern eine unterschiedliche Anzahl von Texturkomponenten aufweist, ist es so, als ob die Texturzuordnung deaktiviert wäre. Die lineare Filterung greift nur in 2D-Texturen auf die vier nächstgelegenen Texturelemente zu. In 1D-Texturen greift die lineare Filterung auf die beiden nächsten Texturelemente zu. Die folgende Funktion ruft Informationen zu **glTexParameterf,** **glTexParameteri,** **glTexParameterfv** und **glTexParameteriv** ab:

[**glGetTexParameter**](glgettexparameter.md)

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





