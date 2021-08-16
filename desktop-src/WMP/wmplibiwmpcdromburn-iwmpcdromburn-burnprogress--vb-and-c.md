---
title: IWMPC wie die burnProgress-Eigenschaft
description: Die burnProgress-Eigenschaft ruft den Fortschritt der CD-Vererbung in Prozent ab.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- burnProgress-Windows Media Player
- burnProgress-Eigenschaft Windows Media Player , IWMPCführungsschnittstelle
- IWMPCwiederSchnittstellenschnittstelle Windows Media Player , burnProgress-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b8e468bc57bb40d990c0b2aeaffc23e184ef2ffa04ab85c9f60cf0d6bced57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332064"
---
# <a name="iwmpcdromburnburnprogress-property"></a>IWMPCwiedrigeEigenschaft::burnProgress

Die **burnProgress-Eigenschaft** ruft den Fortschritt der CD-Vererbung in Prozent ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das der Statuswert ist. Statuswerte liegen zwischen 0 und 100.

## <a name="remarks"></a>Hinweise

Der Statuswert stellt den abgeschlossenen Prozentsatz des gesamten Prozesses dar, einschließlich aller Stagingvorgänge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPCführungsschnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





