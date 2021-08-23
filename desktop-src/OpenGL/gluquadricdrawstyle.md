---
title: gluQuadricDrawStyle-Funktion (Glu.h)
description: Die gluQuadricDrawStyle-Funktion gibt den gewünschten Draw-Stil für Quadrics an.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluQuadricDrawStyle-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a873ed4f4ceaff4aa3dad678dbb4c1fd7a635b0ce41d7a9480af84278c8360c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061558"
---
# <a name="gluquadricdrawstyle-function"></a>gluQuadricDrawStyle-Funktion

Die **gluQuadricDrawStyle-Funktion** gibt den gewünschten Draw-Stil für Quadrics an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*quadObject* 
</dt> <dd>

Das quadrierte Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*Drawstyle* 
</dt> <dd>

Der gewünschte Zeichnen-Stil. Die folgenden Werte sind gültig.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**GLU \_ FILL**</dt> </dl>                   | Quadrics werden mit Polygonprimitiven gerendert. Die Polygone werden im Hinblick auf ihre Normalitäten gegen den Uhrzeigersinn gezeichnet (wie mit [**gluQuadricOrientation**](gluquadricorientation.md)definiert).<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**GLU \_ LINE**</dt> </dl>                   | Quadrische Daten werden als Zeilen gerendert.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**GLU \_ WIEDERERZ**</dt> </dl> | Quadrics werden als Linien gerendert, mit der Ausnahme, dass Kanten, die koplanare Gesichter trennen, nicht gezeichnet werden.<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**GLU \_ POINT**</dt> </dl>                | Quadrics werden als Satz von Punkten gerendert.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **gluQuadricDrawStyle-Funktion** gibt den Draw-Stil für Quadrics an, die mit **quadObject** gerendert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





