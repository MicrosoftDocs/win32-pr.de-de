---
title: IWMPC über die burnFormat-Eigenschaft "BurnFormat"
description: Die burnFormat-Eigenschaft ruft einen Wert ab, der den Typ der zu verwertenden CD angibt.
ms.assetid: f60fcbd2-5d34-46f3-a2e2-29dac2ecf689
keywords:
- burnFormat-Eigenschaft Windows Media Player
- burnFormat-Eigenschaft Windows Media Player , IWMPC über die Schnittstelle
- IWMPC über die Schnittstelle Windows Media Player , burnFormat-Eigenschaft
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
ms.openlocfilehash: 93d5dc4ff27b3650ee37f16a7e90eb535ebe373401363f8c93bd16d09061b7a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000540"
---
# <a name="iwmpcdromburnburnformat-property"></a>IWMPC über die Eigenschaft"::burnFormat"

Die **burnFormat-Eigenschaft** ruft einen Wert ab, der den Typ der zu verwertenden CD angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public WMPBurnFormat burnFormat {get;}
```


```VB

Public ReadOnly Property burnFormat As WMPBurnFormat
```





## <a name="property-value"></a>Eigenschaftswert

Ein **WMPLib.WMP EnumerationFormat,** das ein Wert aus der **WMP Enumeration Ist,** der den Typ der zu verwertenden CD angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                             |
| Namespace<br/> | **WMPLib**<br/>                                                                                          |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib (Interop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPCorpora Überl-Schnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMP Auswendformat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
</dt> </dl>

 

 





