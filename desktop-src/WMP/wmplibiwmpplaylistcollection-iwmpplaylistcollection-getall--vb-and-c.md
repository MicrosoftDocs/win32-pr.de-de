---
title: IWMPPlaylistCollection getAll-Methode
description: Die getAll-Methode gibt eine IWMPPlaylistArray-Schnittstelle zurück, die Zugriff auf alle Wiedergabelisten in der Bibliothek bietet.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- getAll-Methode Windows Media Player
- getAll-Methode Windows Media Player , IWMPPlaylistCollection-Schnittstelle
- IWMPPlaylistCollection-Schnittstelle Windows Media Player , getAll-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ff50c2983d911e7aa3951e34f908d9982b623912539aa4e162c9cccb2f5256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568449"
---
# <a name="iwmpplaylistcollectiongetall-method"></a>IWMPPlaylistCollection::getAll-Methode

Die **getAll-Methode** gibt eine **IWMPPlaylistArray-Schnittstelle** zurück, die Zugriff auf alle Wiedergabelisten in der Bibliothek bietet.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylistArray-Schnittstelle** für das abgerufene Array von Wiedergabelisten.

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player serie 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPPlaylistArray-Schnittstelle (VB und C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection-Schnittstelle (VB und C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





