---
title: Iwmpwiedergabe count (Eigenschaft)
description: Die Count-Eigenschaft ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- Anzahl der Eigenschaften Fenster Media Player
- Count-Eigenschaft, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354703"
---
# <a name="iwmpplaylistcount-property"></a>Iwmpwiedergabe:: count (Eigenschaft)

Die **count** -Eigenschaft ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl der Medienelemente in der Wiedergabeliste ist.

## <a name="remarks"></a>Bemerkungen

Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) -Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





