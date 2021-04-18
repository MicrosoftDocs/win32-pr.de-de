---
title: Iwmpsettings-Balance (Eigenschaft)
description: Die Balance-Eigenschaft ruft den aktuellen Stereo Saldo ab oder legt ihn fest.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Ausgleichen der Eigenschaften Fenster Media Player
- Balance-Eigenschaften Fenster Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows-Media Player, Balance-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354680"
---
# <a name="iwmpsettingsbalance-property"></a>Iwmpsettings:: Balance (Eigenschaft)

Die **Balance** -Eigenschaft ruft den aktuellen Stereo Saldo ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der den Saldo-Wert ist. Dieser Wert kann zwischen 100 und 100 liegen. Der Standardwert ist 0 (null).

## <a name="remarks"></a>Bemerkungen

Der Wert 0 (null) gibt an, dass die Audiodaten gleichzeitig auf dem linken und rechten Kanal abgespielt werden. Der Wert 100 gibt an, dass Audioinhalte nur im linken Kanal abgespielt werden. Der Wert 100 gibt an, dass Audioinhalte nur auf dem rechten Kanal abgespielt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





