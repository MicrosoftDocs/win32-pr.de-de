---
title: glNormal3b-Funktion (Gl.h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3b-Funktion (Gl.h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- glNormal3b-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff27f8082d384c5c244951b5dd237f21cb60875c0912cf742c4f8b2d3ea1f018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358693"
---
# <a name="glnormal3b-function"></a>glNormal3b-Funktion

Legt den aktuellen normalen Vektor fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
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

Die aktuelle Normalität wird immer dann auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3b-Funktion** aufrufen.

Byte-, Short- oder Integerargumente werden mithilfe einer linearen Zuordnung, die den positivsten darstellbaren ganzzahligen Wert 1,0 und der negativste darstellbare ganzzahlige Wert -1,0 zuzuordnen, in das Gleitkommaformat konvertiert.

Normals, die mit **glNormal3b** angegeben werden, benötigen keine Einheitslänge. Wenn die Normalisierung aktiviert ist, werden mit **glNormal3b** angegebene Normalitäten nach der Transformation normalisiert. Sie können die Normalisierung steuern, indem Sie [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL \_ NORMALIZE verwenden. Standardmäßig ist die Normalisierung deaktiviert. Sie können die aktuelle Normalität jederzeit aktualisieren. Insbesondere können Sie **glNormal3b** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufrufen. Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3b ab:**

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

 

 





