---
title: gluquadricnormals-Funktion (glu. h)
description: Die Funktion "gluquadricnormals" gibt an, welche Art von normalen für viercs verwendet werden soll.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- gluquadricnormals-Funktion OpenGL
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
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478018"
---
# <a name="gluquadricnormals-function"></a>gluquadricnormals-Funktion

Die Funktion " **gluquadricnormals** " gibt an, welche Art von normalen für viercs verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*quadobject* 
</dt> <dd>

Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> <dt>

*normale* 
</dt> <dd>

Der gewünschte Typ von normalen. Die folgenden Werte sind gültig.



| Wert                                                                                                                                                | Bedeutung                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <dt>**Glu \_ None**</dt> </dl>       | Es werden keine normale generiert.<br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <dt>**Glu \_ flach**</dt> </dl>       | Eine normale wird für jedes Facetten eines quadkts generiert.<br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <dt>**Glu \_ glatt**</dt> </dl> | Für jeden Scheitelpunkt einer Quadric wird eine normale generiert. Dies ist der Standardwert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gluquadricnormals** " gibt an, welche Art von normalen für mit **quadobject** gerenderten viercs verwendet werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glunewquadric**](glunewquadric.md)
</dt> <dt>

[**gluquadricdrawstyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluquadricorientation**](gluquadricorientation.md)
</dt> <dt>

[**gluquadrictexture**](gluquadrictexture.md)
</dt> </dl>

 

 





