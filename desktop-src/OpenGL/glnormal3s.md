---
title: glNormal3s-Funktion (Gl.h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3s-Funktion (Gl.h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- glNormal3s-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a21ce2ff4c780e19e0849730db5fb7831343a32961e0e673b355124f799c61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795253"
---
# <a name="glnormal3s-function"></a>glNormal3s-Funktion

Legt den aktuellen normalen Vektor fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nx* 
</dt> <dd>

Gibt die x-Koordinate des neuen aktuellen Normalvektors an.

</dd> <dt>

*Ny* 
</dt> <dd>

Gibt die y-Koordinate des neuen aktuellen Normalvektors an.

</dd> <dt>

*Nz* 
</dt> <dd>

Gibt die Z-Koordinate des neuen aktuellen Normalvektors an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die aktuelle Normalität wird auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3s-Funktion** aufrufen.

Byte-, Short- oder Integerargumente werden mit einer linearen Zuordnung, die den positivsten darstellbaren ganzzahligen Wert 1,0 und der negativste darstellbare ganzzahlige Wert -1,0 zuzuordnen, in das Gleitkommaformat konvertiert.

Normals, die mithilfe von **glNormal3s** angegeben werden, benötigen keine Einheitslänge. Wenn die Normalisierung aktiviert ist, werden mit **glNormal3s** angegebene Normalitäten nach der Transformation normalisiert. Sie können die Normalisierung mithilfe von [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL \_ NORMALIZE steuern. Standardmäßig ist die Normalisierung deaktiviert. Sie können die aktuelle Normalität jederzeit aktualisieren. Insbesondere können Sie **glNormal3s** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufrufen. Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3s** ab:

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

 

 





