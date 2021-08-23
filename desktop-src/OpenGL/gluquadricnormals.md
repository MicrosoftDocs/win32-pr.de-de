---
title: gluQuadricNormals-Funktion (Glu.h)
description: Die funktion gluQuadricNormals gibt an, welche Art von Normalitäten für Quadrics verwendet werden sollen.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- gluQuadricNormals-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d535a90f21b88b26c3afd245b2f6350a443fd8915a4cd806df79236484c36d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554180"
---
# <a name="gluquadricnormals-function"></a>gluQuadricNormals-Funktion

Die **funktion gluQuadricNormals** gibt an, welche Art von Normalitäten für Quadrics verwendet werden sollen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*quadObject* 
</dt> <dd>

Das quadrierte Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*Normalen* 
</dt> <dd>

Der gewünschte Typ von Normalitäten. Die folgenden Werte sind gültig.



| Wert                                                                                                                                                | Bedeutung                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <dt>**GLU \_ NONE**</dt> </dl>       | Es werden keine Normalitäten generiert.<br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <dt>**GLU \_ FLAT**</dt> </dl>       | Ein normaler wird für jedes Facet eines Quadric generiert.<br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <dt>**GLU \_ SMOOTH**</dt> </dl> | Für jeden Scheitelpunkt eines Quadrics wird eine Normale generiert. Dies ist der Standardwert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **funktion gluQuadricNormals** gibt an, welche Art von Normalitäten für Quadrics verwendet werden sollen, die mit **quadObject** gerendert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





