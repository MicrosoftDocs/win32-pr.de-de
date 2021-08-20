---
title: glNormal3iv-Funktion (Gl.h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3iv-Funktion (Gl.h)
ms.assetid: cf50e801-a34c-43bd-b7eb-facb84a6472d
keywords:
- glNormal3iv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74db5c09a45fc6b846867b712f15f9b1230e97ee9a4420587e280018b7593b1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795280"
---
# <a name="glnormal3iv-function"></a>glNormal3iv-Funktion

Legt den aktuellen normalen Vektor fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNormal3iv(
   const GLint *v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*V* 
</dt> <dd>

Ein Zeiger auf ein Array von drei Elementen: die x-, y- und z-Koordinaten der neuen aktuellen Normalität.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der aktuelle Normalwert wird auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3iv-Funktion** aufrufen.

Byte-, Short- oder Integerargumente werden in das Gleitkommaformat mit einer linearen Zuordnung konvertiert, die den positivsten darstellbaren ganzzahligen Wert 1,0 und den negativsten darstellbaren ganzzahligen Wert -1,0 zugibt.

Normals, die mit **glNormal3iv angegeben werden,** müssen keine Einheitenlänge haben. Wenn die Normalisierung aktiviert ist, werden die mit **glNormal3iv** angegebenen Normal normalisiert, nachdem die Transformation abgeschlossen wurde. Sie können die Normalisierung steuern, indem [**Sie glEnable und**](glenable.md) [**glDisable mit**](gldisable.md) dem Argument GL \_ NORMALIZE verwenden. Standardmäßig ist die Normalisierung deaktiviert. Sie können den aktuellen Normalwert jederzeit aktualisieren. Insbesondere können Sie **glNormal3iv** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufrufen.**](glend.md) Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3iv ab:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ CURRENT \_ NORMAL

[**glIsEnable mit**](glisenabled.md) argument GL \_ NORMALIZE

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





