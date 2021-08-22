---
title: gluQuadricCallback-Funktion (Glu.h)
description: Die gluQuadricCallback-Funktion definiert einen Rückruf für ein Quadric-Objekt.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluQuadricCallback-Funktion OpenGL
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
ms.openlocfilehash: 36ce32bf041a59f272b18ebe17916963c4e5fd8d208da9d739468c88b9286dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488790"
---
# <a name="gluquadriccallback-function"></a>gluQuadricCallback-Funktion

Die **gluQuadricCallback-Funktion** definiert einen Rückruf für ein Quadric-Objekt.

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

Das Quadric-Objekt (erstellt mit [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*welche* 
</dt> <dd>

Der Rückruf, der definiert wird. Der einzige gültige Wert ist GLU \_ ERROR.



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**\_GLU-FEHLER**</dt> </dl> | Die **gluQuadricCallback-Funktion** wird aufgerufen, wenn ein Fehler auftritt. Das einzelne Argument ist vom Typ **GLenum** und gibt den spezifischen Aufgetretenen Fehler an. Zeichenfolgen, die diese Fehler beschreiben, können mit dem [**gluErrorString-Aufruf abgerufen**](gluerrorstring.md) werden.<br/> |



 

</dd> <dt>

*fn* 
</dt> <dd>

Die funktion, die aufgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden **Sie gluQuadricCallback,** um einen neuen Rückruf zu definieren, der von einem Quadric-Objekt verwendet werden soll. Wenn der angegebene Rückruf bereits definiert ist, wird er ersetzt. Wenn *fn* NULL **ist,** wird jeder vorhandene Rückruf gelöscht.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





