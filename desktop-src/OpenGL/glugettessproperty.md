---
title: gluGetTessProperty-Funktion (Glu.h)
description: Die gluGetTessProperty-Funktion ruft eine Mosaikobjekteigenschaft ab.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- gluGetTessProperty-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d12e7ca8099197b663893b1edcf04dd8fa98348fe4f6d3d324b54f33904e026a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554240"
---
# <a name="glugettessproperty-function"></a>gluGetTessProperty-Funktion

Die **gluGetTessProperty-Funktion** ruft eine Mosaikobjekteigenschaft ab.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tess* 
</dt> <dd>

Das Mosaikobjekt (erstellt mit [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*welche* 
</dt> <dd>

Die Eigenschaft, deren Wert abgerufen werden soll. Die folgenden Werte sind gültig: GLU \_ TESS \_ WINDING \_ RULE, GLU \_ TESS \_ BOUNDARY ONLY und \_ GLU \_ TESS \_ TOLERANCE.

</dd> <dt>

*value* 
</dt> <dd>

Ein Zeiger auf die Position, an der der Wert der benannten Eigenschaft geschrieben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden **Sie gluGetTessProperty,** um Eigenschaften abzurufen, die in einem Mosaikobjekt gespeichert sind. Diese Eigenschaften beeinflussen die Art und Weise, wie Mosaikobjekte interpretiert und gerendert werden. Informationen dazu, was die Eigenschaften sind und was sie tun, finden Sie unter [**gluTessProperty**](glutessproperty.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





