---
title: IWMPSettings balance-Eigenschaft
description: Die Balance-Eigenschaft ruft den aktuellen Stereo-Saldo ab oder legt diese fest.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- balance-Windows Media Player
- balance-Eigenschaft Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , Balance-Eigenschaft
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
ms.openlocfilehash: 76d519d656be6b4974e2b4dd2707aafb2bb153f6b26bafe75de948d5e50c67b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861082"
---
# <a name="iwmpsettingsbalance-property"></a>IWMPSettings::balance-Eigenschaft

Die **Balance-Eigenschaft** ruft den aktuellen Stereo-Saldo ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das der Saldowert ist. Dieser Wert kann zwischen 100 und 100 liegen. Der Standardwert ist 0 (null).

## <a name="remarks"></a>Hinweise

Der Wert 0 (null) gibt an, dass die Audiowiedergabe bei gleicher Lautstärke sowohl auf dem linken als auch auf dem rechten Kanal abgibt. Der Wert 100 gibt an, dass Audio nur im linken Kanal abspielt. Der Wert 100 gibt an, dass Audio nur auf dem richtigen Kanal abspielt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





