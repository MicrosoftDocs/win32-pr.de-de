---
title: IWMPPlaylistCollection remove-Methode
description: Die remove-Methode entfernt eine Wiedergabeliste aus der Bibliothek. | IWMPPlaylistCollection remove-Methode
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- remove-Methode Windows Media Player
- remove-Methode Windows Media Player , IWMPPlaylistCollection-Schnittstelle
- IWMPPlaylistCollection-Schnittstelle Windows Media Player , remove-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b342251bb1885b40d8cd225612ad68b1b54c6ca74cc29a9a934b1fa603837e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745715"
---
# <a name="iwmpplaylistcollectionremove-method"></a>IWMPPlaylistCollection::remove-Methode

Die **remove-Methode** entfernt eine Wiedergabeliste aus der Bibliothek.

## <a name="syntax"></a>Syntax


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pItem* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die Wiedergabeliste, die diese Methode entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Methode benötigen Sie Vollzugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player serie 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection-Schnittstelle (VB und C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





