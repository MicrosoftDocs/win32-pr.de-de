---
title: Iwmpwiedergabe. isidentical (VB und C)
description: Mit der isidentical-Eigenschaft (der get \_ isidentical-Methode in C \) wird ein Wert abgerufen, der angibt, ob die angegebene Wiedergabeliste mit der aktuellen Wiedergabeliste identisch ist.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- Iwmpwiedergabe. isidentical (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee30441e8f0275bba06f71a01095c39da8eae9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364446"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>Iwmpwiedergabe. isidentical (VB und c#)

Mit der **isidentical** -Eigenschaft (der **get \_ isidentical** -Methode in c#) wird ein Wert abgerufen, der angibt, ob die angegebene Wiedergabeliste mit der aktuellen Wiedergabeliste identisch ist.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPPlaylist As IWMPPlaylist
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPPlaylist pIWMPPlaylist
);
```



## <a name="parameters"></a>Parameter

*piwmpwiedergabe Liste*

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die Wiedergabeliste, die diese Methode mit der aktuellen Wiedergabeliste vergleicht.

## <a name="property-value"></a>Eigenschaftswert

Ein **System. boolescher** Wert, der angibt, ob die verglichenen Wiedergabelisten identisch sind.

## <a name="remarks"></a>Bemerkungen

**Iwmpwiedergabe. isidentical** ist eine Eigenschaft in Visual Basic, die einen-Parameter annimmt, während in c# als **iwmpwiedergabe. get \_ isidentical** -Methode bezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





