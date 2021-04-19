---
title: Controls. Step-Methode
description: Die Step-Methode bewirkt, dass das aktuelle Video Medien Element die Wiedergabe für den nächsten Frame oder den vorherigen Frame fixiert.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- Step-Methode (Windows Media Player)
- Step-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, Step-Methode
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
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366044"
---
# <a name="controlsstep-method"></a>Controls. Step-Methode

Die **Step** -Methode bewirkt, dass das aktuelle Video Medien Element die Wiedergabe für den nächsten Frame oder den vorherigen Frame fixiert.

## <a name="syntax"></a>Syntax


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FrameCount* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die angibt, wie viele Frames vor dem Einfrieren durchlaufen werden sollen. Muss derzeit auf 1 oder-1 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode unterstützt derzeit nur die Parameter 1 oder-1, sodass Sie nur einen Frame gleichzeitig ausführen können.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> </dl>

 

 





