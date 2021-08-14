---
title: glMaterialf-Funktion (Gl.h)
description: Die glMaterialf-Funktion gibt Materialparameter für das Beleuchtungsmodell an.
ms.assetid: c6d183c4-2d1f-4fb9-b24f-c132ebfc708d
keywords:
- glMaterialf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMaterialf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aac97cf68996beb5472ff5f11e559af8b58ded31ab12fe5a33ab33d37b13b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358928"
---
# <a name="glmaterialf-function"></a>glMaterialf-Funktion

Die **glMaterialf-Funktion** gibt Materialparameter für das Beleuchtungsmodell an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMaterialf(
   GLenum  face,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* 
</dt> <dd>

Das Gesicht oder die Gesichter, die aktualisiert werden. Dies muss einer der folgenden Sein: GL \_ FRONT, GL \_ BACK oder GL FRONT und GL \_ \_ BACK.

</dd> <dt>

*pname* 
</dt> <dd>

Der einwertige Materialparameter des oder der Gesichter, die aktualisiert werden. Muss \_ GLINESS sein.



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GL-GL-SCHLÄFRIGKEIT**</dt> </dl> | Der *Parameter param* ist ein einzelner Gleitkommawert, der den RGBA-Exponenten des Materials angibt. Ganzzahlige Werte werden direkt zugeordnet. Nur Werte im Bereich \[ 0 und 128 \] werden akzeptiert. Der Standardspezifikations exponent für front- und back-facing materials ist 0. <br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf den der Parameter \_ GLINESS festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                              | Bedeutung                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | Entweder *face* oder *pname* war kein akzeptierter Wert.<br/>                |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | Ein specular-Exponent außerhalb des Bereichs von \[ 0, 128 \] wurde angegeben.<br/> |



## <a name="remarks"></a>Hinweise

Die **glMaterialf-Funktion** weist Materialparametern Werte zu. Es gibt zwei übereinstimmende Sätze von Materialparametern. Eine,  die frontseitige Gruppe, wird verwendet, um Punkte, Linien, Bitmaps und alle Polygone (wenn die zweiseitige Beleuchtung deaktiviert ist) oder einfach frontseitige Polygone zu schattigen (wenn die zweiseitige Beleuchtung aktiviert ist). Die andere Gruppe, *die nach* hinten gerichtet ist, wird nur verwendet, um nach hinten gerichtete Polygone zu beschatten, wenn die zweiseitige Beleuchtung aktiviert ist. Details zu einseitigen und zweiseitigen Beleuchtungsberechnungen finden Sie unter [**glLightModel.**](gllightmodel-functions.md)

Die **glMaterialf-Funktion** verwendet drei Argumente. Die erste, *die Gesichtserkennung,* gibt an, ob die GL FRONT-Materialien, die GL BACK-Materialien oder beide \_ GL FRONT AND \_ \_ \_ \_ BACK-Materialien geändert werden. Der zweite Parameter , *pname,* gibt an, welcher von mehreren Parametern in einer oder beiden Sätzen geändert wird. Der dritte Parameter *( param*) gibt an, welcher Wert dem angegebenen Parameter zugewiesen wird.

Materialparameter werden in der Beleuchtungsgleichung verwendet, die optional auf jeden Scheitelpunkt angewendet wird. Die Gleichung wird in [**glLightModel erläutert.**](gllightmodel-functions.md)

Die Materialparameter können jederzeit aktualisiert werden. Insbesondere kann **glMaterialf** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen werden.**](glend.md) Wenn jedoch nur ein einzelner Materialparameter pro Scheitelpunkt geändert werden soll, wird [**glColorMaterial**](glcolormaterial.md) gegenüber **glMaterialf bevorzugt.**

Die folgende Funktion ruft Informationen im Zusammenhang mit **glMaterialf ab:**

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

 

 





