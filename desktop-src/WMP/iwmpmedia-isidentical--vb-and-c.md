---
title: Iwmpmedia. isidentical (VB und C)
description: Mit der isidentical-Eigenschaft (der get \_ isidentical-Methode in C \) wird ein Wert abgerufen, der angibt, ob das angegebene Medien Element mit dem aktuellen übereinstimmt.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- Iwmpmedia. isidentical (VB und C) Windows Media Player
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
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372201"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>Iwmpmedia. isidentical (VB und c#)

Mit der **isidentical** -Eigenschaft (der **get \_ isidentical** -Methode in c#) wird ein Wert abgerufen, der angibt, ob das angegebene Medien Element mit dem aktuellen übereinstimmt.


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

*piwmpmedia*

Eine **WMPLib. iwmpmedia** -Schnittstelle für das Medien Element, das mit dem aktuellen Medien Element verglichen werden soll.

## <a name="property-value"></a>Eigenschaftswert

Ein **System. Boolean** -Wert, der angibt, ob die beiden Medienelemente identisch sind.

## <a name="remarks"></a>Bemerkungen

**Iwmpmedia. isidentical** ist eine Eigenschaft in Visual Basic, die einen-Parameter annimmt. In c# wird dies als **iwmpmedia. get \_ isidentical** -Methode bezeichnet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **isidentical** -Eigenschaft (die **get \_ isidentical** -Methode in c#) verwendet, um zu überprüfen, ob ein Medien Element mit dem Namen newmedia mit dem aktuellen Medien Element identisch ist. Wenn Sie nicht identisch sind, wird das neue Medien Element wiedergegeben. Andernfalls wird das aktuelle Medium weiterhin ununterbrochen abgespielt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





