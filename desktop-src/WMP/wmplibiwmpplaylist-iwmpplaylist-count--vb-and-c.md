---
title: IWMPPlaylist count-Eigenschaft
description: Die count-Eigenschaft ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- count-Windows Media Player
- count-Eigenschaft Windows Media Player , IWMPPlaylist-Schnittstelle
- IWMPPlaylist-Schnittstelle Windows Media Player , count-Eigenschaft
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
ms.openlocfilehash: aad690278b45563395c926adb4d0329bff8a01c7e8ace2f25ff3fefdb9c39cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568695"
---
# <a name="iwmpplaylistcount-property"></a>IWMPPlaylist::count-Eigenschaft

Die **count-Eigenschaft** ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das die Anzahl der Medienelemente in der Wiedergabeliste ist.

## <a name="remarks"></a>Hinweise

Bevor Sie diese Eigenschaft verwenden können, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

[Beispielcode, der diese](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) Eigenschaft verwendet, finden Sie in der attributeCount-Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





