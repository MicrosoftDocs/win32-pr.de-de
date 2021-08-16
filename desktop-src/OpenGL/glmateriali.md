---
title: glMateriali-Funktion (Gl.h)
description: DieglMateriali-Funktion gibt Materialparameter für das Beleuchtungsmodell an.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- glMateriali-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d850bac6b27672c00dca9b1cafa7b4664dbde5fca0085381b4b166e2106b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358864"
---
# <a name="glmateriali-function"></a>glMateriali-Funktion

Die **glMateriali-Funktion** gibt Materialparameter für das Beleuchtungsmodell an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* 
</dt> <dd>

Das Gesicht oder die Gesichter, die aktualisiert werden. Muss einer der folgenden Sein: GL \_ FRONT, GL \_ BACK oder GL FRONT und GL \_ \_ BACK.

</dd> <dt>

*pname* 
</dt> <dd>

Der einwertige Materialparameter des Gesichts oder der Gesichter, die aktualisiert werden. Muss \_ GLINESS sein.



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GL-VERTRAUENSWÜRDIGKEIT**</dt> </dl> | Der *Parameter param* ist eine einzelne ganze Zahl, die den RGBA-Glanz exponenten des Materials angibt. Ganzzahlige Werte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 128 \] werden akzeptiert. Der Standardspekular exponent für vordere und hintere Materialien ist 0. <br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf den der Parameter GL \_ CABINESS festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                              | Bedeutung                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | Entweder *face* oder *pname* war kein akzeptierter Wert.<br/>                |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | Ein Glanz exponent außerhalb des Bereichs von \[ 0, 128 \] wurde angegeben.<br/> |



## <a name="remarks"></a>Hinweise

Die **glMateriali-Funktion** weist Materialparametern Werte zu. Es gibt zwei übereinstimmende Sätze von Materialparametern. Eine , die *vordere* Gruppe, wird verwendet, um Punkte, Linien, Bitmaps und alle Polygone (wenn die zweiseitige Beleuchtung deaktiviert ist) oder einfach frontseitige Polygone (wenn die zweiseitige Beleuchtung aktiviert ist) zu beschatten. Der andere Satz, *rückwärts gerichtet,* wird nur verwendet, um rückwärts gerichtete Polygone zu schatten, wenn die zweiseitige Beleuchtung aktiviert ist. Ausführliche Informationen zu ein- und zweiseitigen Beleuchtungsberechnungen finden Sie unter [**glLightModel.**](gllightmodel-functions.md)

Die **glMateriali-Funktion** verwendet drei Argumente. Die erste , *face*, gibt an, ob die GL \_ FRONT-Materialien, die GL \_ BACK-Materialien oder beide GL \_ FRONT AND \_ \_ BACK-Materialien geändert werden. Die zweite , *pname*, gibt an, welcher von mehreren Parametern in einem oder beiden Sätzen geändert wird. Der dritte *Parameter* gibt an, welcher Wert dem angegebenen Parameter zugewiesen wird.

Materialparameter werden in der Beleuchtungsgleichung verwendet, die optional auf jeden Scheitelpunkt angewendet wird. Die Gleichung wird in [**glLightModel**](gllightmodel-functions.md)erläutert.

Die Materialparameter können jederzeit aktualisiert werden. Insbesondere kann **glMateriali** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden. Wenn jedoch nur ein einzelner Materialparameter pro Scheitelpunkt geändert werden soll, wird [**glColorMaterial**](glcolormaterial.md) gegenüber **glMateriali** bevorzugt.

Die folgende Funktion ruft Informationen im Zusammenhang mit **glMateriali** ab:

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





