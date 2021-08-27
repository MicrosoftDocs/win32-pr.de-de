---
title: glNormal3i-Funktion (Gl.h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3i-Funktion (Gl.h)
ms.assetid: ea14e5c6-a725-4d24-9a48-c138ee8b6cd1
keywords:
- glNormal3i-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be941d17b63d033ad735b4c13b3d620b77bcf0c376da156341d0a0fd6ca82f1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128100"
---
# <a name="glnormal3i-function"></a>glNormal3i-Funktion

Legt den aktuellen normalen Vektor fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNormal3i(
   GLint nx,
   GLint ny,
   GLint nz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nx* 
</dt> <dd>

Gibt die x-Koordinate für den neuen aktuellen normalen Vektor an.

</dd> <dt>

*Ny* 
</dt> <dd>

Gibt die y-Koordinate für den neuen aktuellen normalen Vektor an.

</dd> <dt>

*Nz* 
</dt> <dd>

Gibt die Z-Koordinate für den neuen aktuellen normalen Vektor an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die aktuelle Normalität wird auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3i-Funktion** aufrufen.

Byte-, Short- oder Integerargumente werden mit einer linearen Zuordnung, die den positivsten darstellbaren ganzzahligen Wert 1,0 und der negativste darstellbare ganzzahlige Wert -1,0 zuzuordnen, in das Gleitkommaformat konvertiert.

Normals, die mit **glNormal3i** angegeben werden, benötigen keine Einheitenlänge. Wenn die Normalisierung aktiviert ist, werden mit **glNormal3i** angegebene Normalitäten nach der Transformation normalisiert. Sie können die Normalisierung steuern, indem Sie [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL \_ NORMALIZE verwenden. Standardmäßig ist die Normalisierung deaktiviert. Sie können die aktuelle Normalität jederzeit aktualisieren. Insbesondere können Sie **glNormal3i** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufrufen. Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3i** ab:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ CURRENT \_ NORMAL

[**glIsEnable**](glisenabled.md) mit dem Argument GL \_ NORMALIZE

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

 

 





