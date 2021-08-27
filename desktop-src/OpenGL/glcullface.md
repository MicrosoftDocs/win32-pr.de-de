---
title: glCullFace-Funktion (Gl.h)
description: Die glCullFace-Funktion gibt an, ob front- oder back-facing Facets gecullt werden können.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- glCullFace-Funktion OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70fd983e9a5921d96ba487f7eb8d6f631b000019e8ff566eb1ecc79e05ce4fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081670"
---
# <a name="glcullface-function"></a>glCullFace-Funktion

Die **glCullFace-Funktion** gibt an, ob front- oder back-facing Facets gecullt werden können.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Gibt an, ob front- oder back-facing Facets Kandidaten für das Culling sind. Die symbolischen Konstanten GL \_ FRONT, GL \_ BACK und GL FRONT AND BACK werden \_ \_ \_ akzeptiert. Der Standardwert ist GL \_ BACK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* war kein akzeptierter Wert.<br/>                                                                                          |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glCullFace-Funktion** gibt an, ob front- oder zurück gerichtete Facets gecullt werden (wie im -Modus *angegeben),* wenn Facet-Culling aktiviert ist. Sie aktivieren und deaktivieren facet culling mit [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL \_ CULL \_ FACE. Facets umfassen Dreiecke, Quadrieren, Polygone und Rechtecke.

Die [**glFrontFace-Funktion**](glfrontface.md) gibt an, welche facets im Uhrzeigersinn und gegen den Uhrzeigersinn nach vorne und nach hinten ausgerichtet sind.

Wenn *der Modus* GL FRONT AND BACK ist, werden keine \_ \_ Facets gezeichnet, aber andere Primitive wie Punkte und \_ Linien werden gezeichnet.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glCullFace ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ CULL \_ FACE \_ MODE

[**glIsEnabled mit**](glisenabled.md) Argument GL \_ CULL \_ FACE

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFrontFace**](glfrontface.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





