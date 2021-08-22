---
title: glStencilFunc-Funktion (Gl.h)
description: Die glStencilFunc-Funktion legt die Funktion und den Verweiswert für Schablonentests fest.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glStencilFunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e529bd83cff8ffb25c8853b7d896926e63982370387f7e2fb5d2ca30a394c1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491510"
---
# <a name="glstencilfunc-function"></a>glStencilFunc-Funktion

Die **glStencilFunc-Funktion** legt die Funktion und den Verweiswert für Schablonentests fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*func* 
</dt> <dd>

Die Testfunktion. Die folgenden acht Token sind gültig.



| Wert                                                                                                                                                   | Bedeutung                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ NEVER**</dt> </dl>          | Fehler immer.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | Übergibt , wenn (*ref*  &  *mask*) < (*Schablonenmaske*  &  ).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Übergibt if (*ref*  &  *mask*) = (*Schablonenmaske*  &  ).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ GREATER**</dt> </dl>    | Übergibt , wenn (*ref*  &  *mask*) > (*Schablonenmaske*  &  ).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Übergibt if (*ref*  &  *mask*) = (*Schablonenmaske*  &  ).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ EQUAL**</dt> </dl>          | Übergibt if (*ref*  &  *mask*) = (*Schablonenmaske*  &  ).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | Übergibt if (*ref*  &  *mask*) ? (*Schablone*  &  *maskieren*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ ALWAYS**</dt> </dl>       | Immer erfolgreich.<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

Der Verweiswert für den Schablonentest. Der *ref-Parameter* ist an den Bereich \[ 0, 2 *n* 1 , \] wobei *n* die Anzahl der Bitebenen im Schablonenpuffer ist.

</dd> <dt>

*mask* 
</dt> <dd>

Eine Maske, die AND ist **und** mit dem Verweiswert und dem gespeicherten Schablonenwert verbunden ist, wenn der Test abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *func* war keiner der acht akzeptierten Werte.<br/>                                                                           |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Schablonierung wie *z*-buffering aktiviert und deaktiviert das Zeichnen pro Pixel. Sie zeichnen die Schablonenebenen mithilfe von OpenGL-Zeichnungsprimitiven, rendern dann Geometrie und Bilder und verwenden die Schablonenebenen, um Teile des Bildschirms zu maskieren. Schablonen werden in der Regel in Mehrpass-Renderingalgorithmen verwendet, um spezielle Effekte zu erzielen, z. B. Decals, Gliederungen und stabiles Solid Geometry Rendering.

Der Schablonentest entfernt bedingt ein Pixel basierend auf dem Ergebnis eines Vergleichs zwischen dem Verweiswert und dem Wert im Schablonenpuffer. Der Test wird durch [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL \_ STENCIL \_ TEST aktiviert. Aktionen, die basierend auf dem Ergebnis des Schablonentests ausgeführt werden, werden mit [**glStencilOp**](glstencilop.md)angegeben.

Der *func-Parameter* ist eine symbolische Konstante, die die Schablonenvergleichsfunktion bestimmt. Sie akzeptiert einen der acht oben gezeigten Werte. Der *ref-Parameter* ist ein ganzzahliger Verweiswert, der im Schablonenvergleich verwendet wird. Er wird an den Bereich \[ 0, 2 *n* 1 und n an die \] Anzahl der Bitebenen im Schablonenpuffer  klammern. Der *mask-Parameter* ist bitweise **AND-ed** mit dem Verweiswert und dem gespeicherten Schablonenwert, wobei die **UND-Werte** am Vergleich beteiligt sind.

Wenn *die Schablone* den Wert darstellt, der am entsprechenden Speicherort des Schablonenpuffers gespeichert ist, zeigt die obige Liste die Auswirkungen jeder Vergleichsfunktion an, die durch *func* angegeben werden kann. Nur wenn der Vergleich erfolgreich ist, wird das Pixel an die nächste Phase des Rasterungsprozesses übergeben (siehe [**glStencilOp**](glstencilop.md)). Alle Tests behandeln *Schablonenwerte* als ganze Zahlen ohne Vorzeichen im Bereich \[ 0, 2 *n* 1, \] wobei *n* die Anzahl der Bitebenen im Schablonenpuffer ist.

Zunächst ist der Schablonentest deaktiviert. Wenn kein Schablonenpuffer vorhanden ist, kann keine Schablonenänderung erfolgen, und es ist so, als ob der Schablonentest immer erfolgreich war.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glStencilFunc** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ STENCIL \_ FUNC

**glGet** mit dem Argument GL \_ STENCIL \_ VALUE \_ MASK

**glGet** mit argument GL \_ STENCIL \_ REF

**glGet** mit argument GL \_ STENCIL \_ BITS

[**glIsEnabled**](glisenabled.md) mit argument GL \_ STENCIL \_ TEST

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





