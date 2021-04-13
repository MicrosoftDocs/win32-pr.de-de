---
title: glugettessproperty-Funktion (glu. h)
description: Die Funktion "glugettessproperty" Ruft eine Mosaik Objekt Eigenschaft ab.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- glugettessproperty-Funktion OpenGL
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
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391812"
---
# <a name="glugettessproperty-function"></a>glugettessproperty-Funktion

Die Funktion " **glugettessproperty** " Ruft eine Mosaik Objekt Eigenschaft ab.

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

*ATI* 
</dt> <dd>

Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).

</dd> <dt>

*,* 
</dt> <dd>

Die Eigenschaft, deren Wert abgerufen werden soll. Die folgenden Werte sind gültig: die \_ Regel "glu Tess" \_ , " \_ glu Tess" und " \_ \_ \_ glu- \_ Toleranz" \_ .

</dd> <dt>

*value* 
</dt> <dd>

Ein Zeiger auf den Speicherort, an dem der Wert der benannten Eigenschaft geschrieben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie " **glugettessproperty** ", um Eigenschaften abzurufen, die in einem Mosaik Objekt gespeichert sind. Diese Eigenschaften beeinflussen die Art und Weise, wie Mosaik Objekte interpretiert und gerendert werden. Informationen zu den Eigenschaften und deren Funktionsfähigkeit finden Sie unter " [**glutessproperty**](glutessproperty.md)".

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

[**glunewtess**](glunewtess.md)
</dt> <dt>

[**glutessproperty**](glutessproperty.md)
</dt> </dl>

 

 





