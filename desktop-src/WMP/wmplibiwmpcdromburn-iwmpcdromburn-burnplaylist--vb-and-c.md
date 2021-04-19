---
title: Iwmpcdromburn burnwiedergabe (Eigenschaft)
description: Die burnwiedergabe-Eigenschaft ruft die aktuelle Wiedergabeliste ab, die auf die CD brennen soll.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- burnwiedergabe-Eigenschaften Fenster Media Player
- burnwiedergabe-Eigenschaft, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, burnwiedergabe (Eigenschaft)
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
ms.openlocfilehash: cae095696b9c106926fb7f363430574b2eb87cea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369132"
---
# <a name="iwmpcdromburnburnplaylist-property"></a>Iwmpcdromburn:: burnwiedergabe (Eigenschaft)

Die **burnwiedergabe** -Eigenschaft ruft die aktuelle Wiedergabeliste ab, die auf die CD brennen soll.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Eigenschaftswert

Die **WMPLib. iwmpwiedergabe** -Schnittstelle der zu brennenden Wiedergabeliste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





