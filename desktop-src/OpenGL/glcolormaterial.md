---
title: glcolormaterial-Funktion (GL. h)
description: Die glcolormaterial-Funktion bewirkt, dass die aktuelle Farbe mit einer Material Farbe nachverfolgt wird.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glcolormaterial-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391994"
---
# <a name="glcolormaterial-function"></a>glcolormaterial-Funktion

Die **glcolormaterial** -Funktion bewirkt, dass die aktuelle Farbe mit einer Material Farbe nachverfolgt wird.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mit* 
</dt> <dd>

Gibt an, ob die Vorder-, Hintergrund-oder beide Vorder-und Hintergrundmaterial Parameter die aktuelle Farbe verfolgen sollen. Akzeptierte Werte sind GL \_ Front, GL \_ Back und GL \_ Front \_ und \_ Back. Der Standardwert ist GL \_ Front \_ und \_ Back.

</dd> <dt>

*mode* 
</dt> <dd>

Gibt an, welche von mehreren Materialparametern die aktuelle Farbe nachverfolgen. Akzeptierte Werte sind GL \_ -Ausgabe, GL \_ Ambient, GL \_ diffus, GL \_ specarität und GL \_ Ambient \_ und \_ diffuse. Der Standardwert ist "GL \_ AMBIENT" und "diffuse" \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Gesichts* -oder *Modus* war kein akzeptierter Wert.<br/>                                                                                |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glcolormaterial** -Funktion gibt an, welche Materialparameter die aktuelle Farbe verfolgen. Wenn Sie das GL- \_ Farb \_ Material aktivieren, wird für jedes Material oder jedes Material, das durch das *Gesicht* angegeben wird, der Materialparameter oder die Parameter, die vom- *Modus* angegeben werden, die aktuelle Farbe jederzeit nachverfolgen. Aktivieren und deaktivieren \_ Sie das GL-Farb \_ Material mit den Funktionen [**glEnable**](glenable.md) und [**gldeaktivieren**](gldisable.md), die Sie mit dem GL- \_ Farb \_ Material als Argument aufzurufen. Standardmäßig ist das GL- \_ Farb \_ Material deaktiviert.

Mit **glcolormaterial** können Sie eine Teilmenge der Materialparameter für jeden Scheitelpunkt mithilfe der Funktion " [**glcolor**](glcolor-functions.md) " ändern, ohne " [**glmaterial**](glmaterial-functions.md)" aufrufen zu müssen. Wenn Sie nur eine solche Teilmenge von Parametern für jeden Scheitelpunkt angeben, ist es besser, dies mit **glcolormaterial** zu tun, als bei **glmaterial**.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glcolormaterial** ab:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Color \_ Material \_ Parameter

**glget** mit dem Argument GL \_ Color \_ Material \_ Face

[**glisenabled**](glisenabled.md) mit dem Argument "GL \_ Color \_ Material"

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

[**gldeaktivieren**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glisenabled**](glisenabled.md)
</dt> <dt>

[**gllight**](gllight-functions.md)
</dt> <dt>

[**gllightmodel**](gllightmodel-functions.md)
</dt> <dt>

[**glmaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





