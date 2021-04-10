---
title: glugetnurbsproperty-Funktion (glu. h)
description: Die Funktion "glugetnurbsproperty" Ruft eine nicht einheitliche Rational B-Spline (NURBS)-Eigenschaft ab.
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- glugetnurbsproperty-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103426"
---
# <a name="glugetnurbsproperty-function"></a>glugetnurbsproperty-Funktion

Die Funktion " **glugetnurbsproperty** " Ruft eine nicht einheitliche Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))-Eigenschaft ab.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> <dt>

*property* 
</dt> <dd>

Die Eigenschaft, deren Wert abgerufen werden soll. Die folgenden Werte sind gültig: glu \_ - \_ samplingtoleranz, Glu- \_ Anzeige \_ Modus, Glu \_ -culult, Glu- \_ automatische \_ Lade \_ Matrix, Glu- \_ parametrimetrische \_ Toleranz, Glu- \_ Samplingmethode \_ , Glu \_ U \_ Step und glu \_ V \_ Step.

</dd> <dt>

*value* 
</dt> <dd>

Ein Zeiger auf den Speicherort, in den der Wert der benannten Eigenschaft geschrieben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie " **glugetnurbsproperty** ", um in einem nurb-Objekt gespeicherte Eigenschaften abzurufen. Diese Eigenschaften wirken sich auf die Darstellung von nursb-Kurven und-Flächen aus. Informationen zu den Eigenschaften von nurb finden Sie unter [**glunurbsproperty**](glunurbsproperty.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**glunurbsproperty**](glunurbsproperty.md)
</dt> </dl>

 

 





