---
title: IWMPC über die burnPlaylist-Eigenschaft "burnPlaylist"
description: Die burnPlaylist-Eigenschaft ruft die aktuelle Wiedergabeliste ab, die auf die CD geschrieben werden soll.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- burnPlaylist-Eigenschaft Windows Media Player
- burnPlaylist-Eigenschaft Windows Media Player , IWMPCakuSer-Schnittstelle
- IWMPC über die Schnittstelle Windows Media Player , burnPlaylist-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnPlaylist
- IWMPCdromBurn.get_burnPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 186996632a5b25c89019f9bbb692d9804ae33130650d4b0a29c0cb51e30d0792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116593"
---
# <a name="iwmpcdromburnburnplaylist-property"></a>IWMPC über die Eigenschaft"::burnPlaylist"

Die **burnPlaylist-Eigenschaft** ruft die aktuelle Wiedergabeliste ab, die auf die CD geschrieben werden soll.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Eigenschaftswert

Die **WMPLib.IWMPPlaylist-Schnittstelle** der Wiedergabeliste, die zusammengestellt werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPCorpora Überl-Schnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





