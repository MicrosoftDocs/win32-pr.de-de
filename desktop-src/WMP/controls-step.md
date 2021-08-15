---
title: Controls.step-Methode
description: Die Schrittmethode bewirkt, dass das aktuelle Videomedienelement die Wiedergabe im nächsten oder vorherigen Frame einfriert.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- step-Methode Windows Media Player
- step-Methode Windows Media Player , Controls-Klasse
- Controls-Klasse Windows Media Player , Step-Methode
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4626ff80aee55ad6c22be7580a07ef2319afb6792a8c11b815d72af23b5727fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839825"
---
# <a name="controlsstep-method"></a>Controls.step-Methode

Die **Schrittmethode** bewirkt, dass das aktuelle Videomedienelement die Wiedergabe im nächsten oder vorherigen Frame einfriert.

## <a name="syntax"></a>Syntax


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*frameCount* \[ In\]
</dt> <dd>

**Number** (**long**), die angibt, wie viele Frames vor dem Einfrieren geschritten werden sollen. Muss derzeit auf 1 oder -1 festgelegt sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode unterstützt derzeit nur die Parameter 1 oder -1, sodass Sie jeweils nur einen Frame schrittweise verwenden können.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> </dl>

 

 





