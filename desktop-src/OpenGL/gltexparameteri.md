---
title: glTexParameteri-Funktion (Gl.h)
description: Legt Texturparameter fest. | glTexParameteri-Funktion (Gl.h)
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
keywords:
- glTexParameteri-Funktion OpenGL
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
ms.openlocfilehash: 3bcc269c92d2d233f8c0dae89438232830539c3f8f59c3f8e28ef2be6ba42e54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613237"
---
# <a name="gltexparameteri-function"></a>glTexParameteri-Funktion

Legt Texturparameter fest.

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

Die Zieltextur, die entweder GL \_ TEXTURE \_ 1D oder GL \_ TEXTURE \_ 2D sein muss.

</dd> <dt>

*pname* 
</dt> <dd>

Der symbolische Name eines einwertigen Texturparameters. Die folgenden Symbole werden in *pname* akzeptiert.



| Wert                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**GL \_ TEXTURE \_ MIN \_ FILTER**</dt> </dl> | Die Texturverkleinerungsfunktion wird immer dann verwendet, wenn das zu texturierende Pixel einem Bereich zugeordnet wird, der größer als ein Texturelement ist. Es gibt sechs definierte Vergrößerungsfunktionen. Zwei von ihnen verwenden das nächste oder die nächsten vier Texturelemente, um den Texturwert zu berechnen. Die anderen vier verwenden Mipmaps. <br/> Eine Mipmap ist eine geordnete Gruppe von Arrays, die das gleiche Bild mit progressiv niedrigeren Auflösungen darstellen. Wenn die Textur die Abmessungen 2nx2<sup>m</sup> aufweist, gibt es max(n, m) + 1 mipmaps. Die erste Mipmap ist die ursprüngliche Textur mit den Abmessungen 2nx2<sup>m</sup>. Jede nachfolgende Mipmap hat die Abmessungen 2<sup>k</sup>1x2<sup>l</sup>1, wobei 2<sup>k</sup>x2<sup>l</sup> die Dimensionen der vorherigen Mipmap sind, bis entweder k = 0 oder l = 0 ist. An diesem Punkt haben nachfolgende Mipmaps die Dimension 1x2<sup>l</sup>1 oder 2<sup>k</sup>1x1 bis zur endgültigen Mipmap, die die Dimension 1x1 aufweist. Mipmaps werden [**mithilfe von glTexImage1D**](glteximage1d.md) oder [**glTexImage2D**](glteximage2d.md) mit dem Detailebenenargument definiert, das die Reihenfolge der Mipmaps angibt. Ebene 0 ist die ursprüngliche Textur. level bold max(n, m) ist die endgültige 1x1-Mipmap.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**GL \_ TEXTURE \_ MAG \_ FILTER**</dt> </dl> | Die Texturvergrößerungsfunktion wird verwendet, wenn das texturierte Pixel einem Bereich zugeordnet wird, der kleiner oder gleich einem Texturelement ist. Die Texturvergrößerungsfunktion wird entweder auf GL \_ NEAREST oder GL \_ LINEAR festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>             | Legt den Wrap-Parameter für Texturkoordinaten entweder auf GL \_ WRAP oder GL REPEAT \_ fest. GL WRAP bewirkt, dass die Koordinaten von an \_ den Bereich 0,1 angeklammern werden, und ist nützlich, um das \[ \] Umschließen von Artefakten zu verhindern, wenn ein einzelnes Bild einem Objekt zugeordnet wird. GL \_ REPEAT bewirkt, dass der ganzzahlige Teil der -Koordinate ignoriert wird. OpenGL verwendet nur den Bruchteil, wodurch ein sich wiederholendes Muster erstellt wird. Auf Rahmentexturelemente wird nur zugegriffen, wenn wrapping auf GL WRAP festgelegt \_ ist. Zunächst wird GL \_ TEXTURE WRAP S auf GL REPEAT \_ \_ \_ festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>             | Legt den Wrap-Parameter für die Texturkoordinate t entweder auf GL \_ WRAP oder GL REPEAT \_ fest. Weitere Informationen finden Sie in der Diskussion unter GL \_ TEXTURE \_ WRAP \_ S. Zunächst ist GL \_ TEXTURE WRAP T auf GL \_ \_ REPEAT festgelegt. \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert von *pname*.

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



## <a name="see-also"></a>Weitere Informationen

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

 

 





