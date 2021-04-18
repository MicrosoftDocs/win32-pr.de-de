---
title: IWMPControls2 Step-Methode
description: Die Step-Methode bewirkt, dass das aktuelle Video Medien Element in den nächsten Frame oder den vorherigen Frame geht und die Wiedergabe fixiert.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- Step-Methode (Windows Media Player)
- Step-Methode, Windows Media Player, IWMPControls2-Schnittstelle
- IWMPControls2 Interface, Windows Media Player, Step-Methode
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371747"
---
# <a name="iwmpcontrols2step-method"></a>IWMPControls2:: Step-Methode

Die **Step** -Methode bewirkt, dass das aktuelle Video Medien Element in den nächsten Frame oder den vorherigen Frame geht und die Wiedergabe fixiert.

## <a name="syntax"></a>Syntax


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*LStep* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der angibt, wie viele Frames vor dem Einfrieren durchlaufen werden. Muss auf 1 oder-1 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode unterstützt derzeit nur die Parameter 1 oder-1, sodass Sie nur einen Frame gleichzeitig ausführen können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls2-Schnittstelle (VB und c#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Iwmpdvd-Schnittstelle (VB und c#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





