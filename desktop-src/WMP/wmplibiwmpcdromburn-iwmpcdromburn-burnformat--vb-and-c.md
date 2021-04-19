---
title: Iwmpcdromburn burnformat (Eigenschaft)
description: Die burnformat-Eigenschaft ruft einen Wert ab, der den Typ der zu brennenden CD angibt.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- burnformat-Eigenschaften Fenster Media Player
- burnformat-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, burnformat (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnFormat
- IWMPCdromBurn.get_burnFormat
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17e379727376b1ce272a95cd77c688fa611b291a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361327"
---
# <a name="iwmpcdromburnburnformat-property"></a>Iwmpcdromburn:: burnformat (Eigenschaft)

Die **burnformat** -Eigenschaft ruft einen Wert ab, der den Typ der zu brennenden CD angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a>Eigenschaftswert

Ein **WMPLib. wmpburnformat** , bei dem es sich um einen Wert aus der **wmpburnformat** -Enumeration handelt, der den Typ der zu brennenden CD angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                             |
| Namespace<br/> | **WMPLib**<br/>                                                                                          |
| Assembly<br/>  | <dl> <dt>Interop. WMPLib (Interop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Wmpburnformat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





