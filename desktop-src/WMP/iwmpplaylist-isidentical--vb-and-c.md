---
title: IWMPPlaylist.isIdentical (VB und C )
description: Die isIdentical-Eigenschaft (die get isIdentical-Methode in C\ ) ruft einen Wert ab, der angibt, ob die angegebene Wiedergabeliste mit der \_ aktuellen Wiedergabeliste identisch ist.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- IWMPPlaylist.isIdentical (VB und C ) Windows Media Player
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
ms.openlocfilehash: eca62b1667250b049cf47e797d59bdddea0444c6ea8803ca0fc8daf526289eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119009"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>IWMPPlaylist.isIdentical (VB und C#)

Die **isIdentical-Eigenschaft** **(die get \_ isIdentical-Methode** in C#) ruft einen Wert ab, der angibt, ob die angegebene Wiedergabeliste mit der aktuellen Wiedergabeliste identisch ist.


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

*pIWMPPlaylist*

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die Wiedergabeliste, die diese Methode mit der aktuellen Wiedergabeliste vergleicht.

## <a name="property-value"></a>Eigenschaftswert

Ein **System.Boolean-Wert,** der angibt, ob die verglichenen Wiedergabelisten identisch sind.

## <a name="remarks"></a>Hinweise

**IWMPPlaylist.isIdentical** ist eine Eigenschaft in Visual Basic, die einen Parameter akzeptiert, während sie in C# als **IWMPPlaylist.get \_ isIdentical-Methode** bezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





