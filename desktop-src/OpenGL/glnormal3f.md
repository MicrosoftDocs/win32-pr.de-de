---
title: glNormal3f-Funktion (GL. h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3f-Funktion (GL. h)
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- glNormal3f-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e83b874b1588ad8bd91da9e5c9f831062de9cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361160"
---
# <a name="glnormal3f-function"></a>glNormal3f-Funktion

Legt den aktuellen normalen Vektor fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NX* 
</dt> <dd>

Gibt die x-Koordinate für den neuen aktuellen normalen Vektor an.

</dd> <dt>

*geile* 
</dt> <dd>

Gibt die y-Koordinate für den neuen aktuellen normalen Vektor an.

</dd> <dt>

*NZ* 
</dt> <dd>

Gibt die z-Koordinate für den neuen aktuellen normalen Vektor an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der aktuelle Normalwert ist auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3f** -Funktion aufzurufen.

Byte-, kurz-oder ganzzahlige Argumente werden in das Gleit Komma Format mit einer linearen Zuordnung konvertiert, die den positivsten darstellbaren ganzzahligen Wert 1,0 und den am meisten negativen darstellbaren ganzzahligen Wert zu-1,0 zuordnet.

Mit **glNormal3f** angegebene normale müssen keine Einheitslänge aufweisen. Wenn Normalisierung aktiviert ist, werden normale, die mit **glNormal3f** angegeben werden, nach der Transformation normalisiert. Sie können die Normalisierung mithilfe von [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md) mit dem Argument GL \_ normalize steuern. Standardmäßig ist die Normalisierung deaktiviert. Sie können die aktuelle Normalzeit jederzeit aktualisieren. Vor allem können Sie **glNormal3f** zwischen einem " [**glBegin**](glbegin.md) "-Befehl und dem entsprechenden " [**glEnd**](glend.md)"-Aufrufe aufzurufen. Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3f** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Current \_ Normal

[**glisenable**](glisenabled.md) mit dem Argument GL \_ normalize

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glcolor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glindex**](glindex-functions.md)
</dt> <dt>

[**gltexcoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





