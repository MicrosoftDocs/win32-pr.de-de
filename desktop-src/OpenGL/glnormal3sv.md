---
title: glNormal3sv-Funktion (Gl.h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3sv-Funktion (Gl.h)
ms.assetid: 59cdebc9-594a-429f-ba5d-7c63a533cc11
keywords:
- glNormal3sv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec60f7fec008d23bf40667d897a1fc4e24ecb92ada7210ef79b3788610067d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795243"
---
# <a name="glnormal3sv-function"></a>glNormal3sv-Funktion

Legt den aktuellen normalen Vektor fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNormal3sv(
   const GLshort *v
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

Der aktuelle Normalwert wird auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3sv-Funktion** aufrufen.

Byte-, Short- oder Integerargumente werden in das Gleitkommaformat mit einer linearen Zuordnung konvertiert, die den positivsten darstellbaren ganzzahligen Wert 1,0 und den negativsten darstellbaren ganzzahligen Wert -1,0 zugibt.

Normals, die mit **glNormal3sv angegeben werden,** müssen keine Einheitenlänge haben. Wenn die Normalisierung aktiviert ist, werden die mit **glNormal3sv** angegebenen Normal normalisiert. Sie können die Normalisierung steuern, indem [**Sie glEnable**](glenable.md) und [**glDisable mit**](gldisable.md) dem Argument GL \_ NORMALIZE verwenden. Standardmäßig ist die Normalisierung deaktiviert. Sie können den aktuellen Normalwert jederzeit aktualisieren. Insbesondere können Sie **glNormal3sv zwischen** einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufrufen.**](glend.md) Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3sv ab:**

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

 

 





