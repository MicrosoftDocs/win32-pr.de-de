---
title: Iwmpcdromrip-ripstate (Eigenschaft)
description: Die ripstate-Eigenschaft ruft einen Enumerationswert ab, der den aktuellen Zustand des einreißen-Prozesses angibt.
ms.assetid: eacf36d9-725c-47cf-9f90-6241feeb67bc
keywords:
- ripstate-Eigenschaften Fenster Media Player
- ripstate-Eigenschaft, Windows Media Player, iwmpcdromrip-Schnittstelle
- Iwmpcdromrip-Schnittstelle, Windows Media Player, ripstate (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripState
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ea8ff7d863faa1f44c8d0578777ae6cd605
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373817"
---
# <a name="iwmpcdromripripstate-property"></a>Iwmpcdromrip:: ripstate (Eigenschaft)

Die **ripstate** -Eigenschaft ruft einen Enumerationswert ab, der den aktuellen Zustand des einreißen-Prozesses angibt.

## <a name="syntax"></a>Syntax


```CSharp
public WMPRipState ripState {get; set;}
```


```VB

Public ReadOnly Property ripState As WMPRipState
```





## <a name="property-value"></a>Eigenschaftswert

Ein **WMPLib. wmpripstate** , bei dem es sich um einen Wert aus der **wmpripstate** -Enumeration handelt, der den aktuellen Zustand angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromrip-Schnittstelle (VB und c#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Ripping einer CD**](ripping-a-cd.md)
</dt> <dt>

[**Wmpripstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





