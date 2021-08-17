---
title: glNormal3fv-Funktion (Gl.h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3fv-Funktion (Gl.h)
ms.assetid: 8e501de8-5877-4d77-9f32-4596d5217636
keywords:
- glNormal3fv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cbaf9cea7c8e0955597a3893e5ad999735c2f9457092c833eb40e71cb462f07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795469"
---
# <a name="glnormal3fv-function"></a>glNormal3fv-Funktion

Legt den aktuellen normalen Vektor fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNormal3fv(
   const GLfloat *v
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

Die aktuelle Normalität wird auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3fv-Funktion** aufrufen.

Byte-, Short- oder Integerargumente werden mit einer linearen Zuordnung, die den positivsten darstellbaren ganzzahligen Wert 1,0 und der negativste darstellbare ganzzahlige Wert -1,0 zuzuordnen, in das Gleitkommaformat konvertiert.

Normals, die mit **glNormal3fv** angegeben werden, benötigen keine Einheitenlänge. Wenn die Normalisierung aktiviert ist, werden mit **glNormal3fv** angegebene Normalitäten nach der Transformation normalisiert. Sie können die Normalisierung steuern, indem Sie [**glEnable**](glenable.md) und [**glDisable**](gldisable.md) mit dem Argument GL \_ NORMALIZE verwenden. Standardmäßig ist die Normalisierung deaktiviert. Sie können die aktuelle Normale jederzeit aktualisieren. Insbesondere können Sie **glNormal3fv** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufrufen. Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3fv ab:**

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

 

 





