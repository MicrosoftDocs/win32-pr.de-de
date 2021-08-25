---
title: IWMPC wie burnState (Eigenschaft)
description: Die burnState-Eigenschaft ruft einen Enumerationswert ab, der den aktuellen Burn-Zustand angibt.
ms.assetid: 2bb543f9-9e4c-4425-99d6-ac89ef7f5807
keywords:
- burnState-Windows Media Player
- burnState-Eigenschaft Windows Media Player , IWMPC wie die Schnittstelle
- IWMPCwiederSchnittstellenschnittstelle Windows Media Player , burnState-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnState
- IWMPCdromBurn.get_burnState
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871d0884c9e5bf60a666f299953cff77d9a458b5a56f505c0588fafdb740023b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862040"
---
# <a name="iwmpcdromburnburnstate-property"></a>IWMPCwiedrig::burnState-Eigenschaft

Die **burnState-Eigenschaft** ruft einen Enumerationswert ab, der den aktuellen Burn-Zustand angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public WMPBurnState burnState {get;}
```


```VB

Public ReadOnly Property burnState As WMPBurnState
```





## <a name="property-value"></a>Eigenschaftswert

Ein **WMPLib.WMPMemberState,** der ein Wert aus der **WMP-Enumeration ist,** der den aktuellen Zustand angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPCführungsschnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMP-Zustand**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





