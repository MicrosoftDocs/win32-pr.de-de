---
title: gluvierccallback-Funktion (glu. h)
description: Die Funktion "gluvierccallback" definiert einen Rückruf für ein Quadric-Objekt.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluvierccallback-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518413"
---
# <a name="gluquadriccallback-function"></a>gluvierccallback-Funktion

Die Funktion " **gluvierccallback** " definiert einen Rückruf für ein Quadric-Objekt.

## <a name="syntax"></a>Syntax


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*qobj* 
</dt> <dd>

Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).

</dd> <dt>

*,* 
</dt> <dd>

Der Rückruf, der definiert wird. Der einzige gültige Wert ist "glu \_ Error".



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**Glu- \_ Fehler**</dt> </dl> | Die Funktion " **gluvierccallback** " wird aufgerufen, wenn ein Fehler auftritt. Das einzige Argument ist vom Typ " **GLenum**" und gibt den spezifischen Fehler an, der aufgetreten ist. Zeichen folgen, die diese Fehler beschreiben, können mit dem " [**gluerrorstring**](gluerrorstring.md) "-Befehl abgerufen werden.<br/> |



 

</dd> <dt>

*fn* 
</dt> <dd>

Die aufzurufende Funktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie " **gluvierccallback** ", um einen neuen Rückruf zu definieren, der von einem Quadric-Objekt verwendet werden soll. Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt. Wenn *FN* den Wert **null** hat, wird ein beliebiger vorhandener Rückruf gelöscht.

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

[**glunewquadric**](glunewquadric.md)
</dt> </dl>

 

 





