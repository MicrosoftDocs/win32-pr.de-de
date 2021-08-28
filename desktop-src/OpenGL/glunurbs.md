---
title: gluNurbsCallback-Funktion (Glu.h)
description: Die funktion gluNurbsCallback definiert einen Rückruf für ein NURBS-Objekt (Non-Uniform Rational B-Spline).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- gluNurbsCallback-Funktion OpenGL
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
ms.openlocfilehash: d1da7ebc999d44911cb345b051213a12865e608db7b7fe66e33eb1bb567ef7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519500"
---
# <a name="glunurbscallback-function"></a>gluNurbsCallback-Funktion

Die **gluNurbsCallback-Funktion** definiert einen Rückruf für ein nicht einheitliches rationales B-Spline-Objekt [(NURBS).](using-nurbs-curves-and-surfaces.md)

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

Das NURBS-Objekt (erstellt mit [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*welche* 
</dt> <dd>

Der rückruf, der definiert wird. Der einzige gültige Wert ist GLU \_ ERROR. Die Bedeutung von GLU \_ ERROR bedeutet, dass die Fehlerfunktion aufgerufen wird, wenn ein Fehler auftritt. Das einzelne Argument ist vom Typ **GLenum** und gibt den spezifischen Fehler an, der aufgetreten ist. Es gibt 37 Fehler, die nur für NURBS gelten. Diese werden glu \_ nurbs \_ error1 bis GLU \_ NURBS \_ ERROR37 genannt. Zeichenfolgen, die diese Fehler beschreiben, können mit [**gluErrorString**](gluerrorstring.md)abgerufen werden.

</dd> <dt>

*fn* 
</dt> <dd>

Ein Zeiger auf die Rückruffunktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie **gluNurbsCallback,** um einen Rückruf zu definieren, der von einem NURBS-Objekt verwendet werden soll. Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt. Wenn *fn* **NULL** ist, wird jeder vorhandene Rückruf gelöscht.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





