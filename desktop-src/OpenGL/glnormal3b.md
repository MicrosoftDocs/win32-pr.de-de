---
title: glNormal3b-Funktion (GL. h)
description: Legt den aktuellen normalen Vektor fest. | glNormal3b-Funktion (GL. h)
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
ms.openlocfilehash: 3a09a92b718881670ed5625fd5aa94a23193cdd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869708"
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

Der aktuelle Normalwert ist auf die angegebenen Koordinaten festgelegt, wenn Sie die **glNormal3b** -Funktion aufzurufen.

Byte-, kurz-oder ganzzahlige Argumente werden in das Gleit Komma Format konvertiert, indem eine lineare Zuordnung verwendet wird, die den positivsten darstellbaren ganzzahligen Wert 1,0 und den negativsten darstellbaren ganzzahligen Wert zu-1,0 zuordnet.

Mit **glNormal3b** angegebene normale müssen keine Einheitslänge aufweisen. Wenn Normalisierung aktiviert ist, werden normale, die mit **glNormal3b** angegeben werden, nach der Transformation normalisiert. Sie können die Normalisierung mithilfe von [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md) mit dem Argument GL \_ normalize steuern. Standardmäßig ist die Normalisierung deaktiviert. Sie können die aktuelle Normalzeit jederzeit aktualisieren. Vor allem können Sie **glNormal3b** zwischen einem " [**glBegin**](glbegin.md) "-Befehl und dem entsprechenden " [**glEnd**](glend.md)"-Aufrufe aufzurufen. Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glNormal3b** ab:

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

 

 





