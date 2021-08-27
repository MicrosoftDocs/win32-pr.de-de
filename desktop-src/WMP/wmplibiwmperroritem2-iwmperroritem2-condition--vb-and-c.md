---
title: IWMPErrorItem2-Bedingungseigenschaft
description: Die Condition-Eigenschaft ruft einen Wert ab, der die Bedingung für den Fehler angibt.
ms.assetid: 68800d75-8341-40d1-b699-ffe27bb1f38a
keywords:
- Condition-Windows Media Player
- condition-Windows Media Player , IWMPErrorItem2-Schnittstelle
- IWMPErrorItem2-Schnittstelle Windows Media Player , Bedingungseigenschaft
topic_type:
- apiref
api_name:
- IWMPErrorItem2.condition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f964a94ed4e1b3b3c86fc1498ce6b8e950b8b7b571be91d297b32247fb3c391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122610"
---
# <a name="iwmperroritem2condition-property"></a>IWMPErrorItem2::condition-Eigenschaft

Die **Condition-Eigenschaft** ruft einen Wert ab, der die Bedingung für den Fehler angibt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 condition {get; set;}
```


```VB

Public ReadOnly Property condition As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das der Bedingungscode ist.

## <a name="remarks"></a>Hinweise

Der Bedingungscode ist ein Wert, der von Microsoft verwendet wird, um zusätzliche Informationen für technische Supportmitarbeiter zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPErrorItem2-Schnittstelle (VB und C#)**](iwmperroritem2--vb-and-c.md)
</dt> </dl>

 

 





