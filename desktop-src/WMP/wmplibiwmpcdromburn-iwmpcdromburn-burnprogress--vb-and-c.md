---
title: Iwmpcdromburn-burnprogress (Eigenschaft)
description: Die burnprogress-Eigenschaft ruft den Fortschritt der CD-brennen als Prozentsatz ab.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- burnprogress-Eigenschaften Fenster Media Player
- burnprogress-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, burnprogress (Eigenschaft)
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
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372580"
---
# <a name="iwmpcdromburnburnprogress-property"></a>Iwmpcdromburn:: burnprogress (Eigenschaft)

Die **burnprogress** -Eigenschaft ruft den Fortschritt der CD-brennen als Prozentsatz ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der der Fortschritts Wert ist. Die Statuswerte liegen im Bereich von 0 bis 100.

## <a name="remarks"></a>Bemerkungen

Der Statuswert stellt den abgeschlossenen Prozentsatz des gesamten Brennvorgangs dar, einschließlich aller stagingvorgänge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





