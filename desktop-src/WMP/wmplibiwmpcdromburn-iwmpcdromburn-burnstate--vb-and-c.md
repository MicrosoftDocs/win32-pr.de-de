---
title: Iwmpcdromburn burnstate (Eigenschaft)
description: Die burnstate-Eigenschaft ruft einen Enumerationswert ab, der den aktuellen Brenn Zustand angibt.
ms.assetid: 2bb543f9-9e4c-4425-99d6-ac89ef7f5807
keywords:
- burnstate-Eigenschaften Fenster Media Player
- burnstate-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, burnstate (Eigenschaft)
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
ms.openlocfilehash: 2c6b1aa8ec39f032e8f130a75370131bd2894c64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360897"
---
# <a name="iwmpcdromburnburnstate-property"></a>Iwmpcdromburn:: burnstate (Eigenschaft)

Die **burnstate** -Eigenschaft ruft einen Enumerationswert ab, der den aktuellen Brenn Zustand angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public WMPBurnState burnState {get;}
```


```VB

Public ReadOnly Property burnState As WMPBurnState
```





## <a name="property-value"></a>Eigenschaftswert

Ein **WMPLib. wmpburnstate** , bei dem es sich um einen Wert aus der **wmpburnstate** -Enumeration handelt, der den aktuellen Zustand angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Wmpburnstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





