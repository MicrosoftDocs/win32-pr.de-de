---
title: glunurbscallback-Funktion (glu. h)
description: Die Funktion "glunurbscallback" definiert einen Rückruf für ein nicht einheitliches Rational B-Spline-Objekt (NURBS).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- glunurbscallback-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342414"
---
# <a name="glunurbscallback-function"></a>glunurbscallback-Funktion

Die Funktion " **glunurbscallback** " definiert einen Rückruf für ein nicht einheitliches Rational B-Spline-Objekt ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nobj* 
</dt> <dd>

Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).

</dd> <dt>

*,* 
</dt> <dd>

Der Rückruf, der definiert wird. Der einzige gültige Wert ist "glu \_ Error". Die Bedeutung von "glu \_ Error" bedeutet, dass die Fehlerfunktion aufgerufen wird, wenn ein Fehler auftritt. Das einzige Argument ist vom Typ " **GLenum**" und gibt den spezifischen Fehler an, der aufgetreten ist. Es gibt 37-Fehler, die für nursb eindeutig sind, mit dem Namen "glu \_ nursb \_ ERROR1 through glu \_ nursb \_ ERROR37". Zeichen folgen, die diese Fehler beschreiben, können mit " [**gluerrorstring**](gluerrorstring.md)" abgerufen werden.

</dd> <dt>

*fn* 
</dt> <dd>

Ein Zeiger auf die Rückruffunktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **glunurbscallback** , um einen Rückruf zu definieren, der von einem nurb-Objekt verwendet werden soll. Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt. Wenn *FN* **null** ist, wird ein beliebiger vorhandener Rückruf gelöscht.

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

[**gluerrorstring**](gluerrorstring.md)
</dt> <dt>

[**glunewnurbsrenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





