---
title: IWMPMedia.isIdentical (VB und C )
description: Die isIdentical-Eigenschaft (die get \_ isIdentical-Methode in C\) ruft einen Wert ab, der angibt, ob das angegebene Medienelement mit dem aktuellen Element identisch ist.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia.isIdentical (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e8de133003bdddcf0438e5a13dc3fa74227ede7bf42350e2b7c3c96f2c197e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003580"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia.isIdentical (VB und C#)

Die **isIdentical-Eigenschaft** (die **get \_ isIdentical-Methode** in C#) ruft einen Wert ab, der angibt, ob das angegebene Medienelement mit dem aktuellen Element identisch ist.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a>Parameter

*pIWMPMedia*

Eine **WMPLib.IWMPMedia-Schnittstelle** zum Medienelement, das mit dem aktuellen Medienelement verglichen werden soll.

## <a name="property-value"></a>Eigenschaftswert

Ein **System.Boolean-Wert,** der angibt, ob die beiden Medienelemente identisch sind.

## <a name="remarks"></a>Hinweise

**IWMPMedia.isIdentical** ist eine Eigenschaft in Visual Basic, die einen Parameter annimmt. In C# wird dies als **IWMPMedia.get \_ isIdentical-Methode** bezeichnet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **isIdentical-Eigenschaft** (die **get \_ isIdentical-Methode** in C#) verwendet, um zu überprüfen, ob ein Medienelement namens newMedia mit dem aktuellen Medienelement identisch ist. Wenn sie nicht identisch sind, wird das neue Medienelement wiedergegeben. Andernfalls werden die aktuellen Medien weiterhin ununterbrochen wiedergegeben. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





