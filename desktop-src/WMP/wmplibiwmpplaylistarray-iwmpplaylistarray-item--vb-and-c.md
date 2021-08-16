---
title: IWMPPlaylistArray Item-Methode
description: Die Item-Methode gibt eine IWMPPlaylist-Schnittstelle zurück, die die Wiedergabeliste am angegebenen Index darstellt.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Item-Methode Windows Media Player
- Item-Methode Windows Media Player , IWMPPlaylistArray-Schnittstelle
- IWMPPlaylistArray-Schnittstelle Windows Media Player , Item-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e73614e1ef00f29d6b09d3d49e2c7e514bae807245f00f30f4d3382d8f1a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331159"
---
# <a name="iwmpplaylistarrayitem-method"></a>IWMPPlaylistArray::Item-Methode

Die **Item-Methode** gibt eine **IWMPPlaylist-Schnittstelle** zurück, die die Wiedergabeliste am angegebenen Index darstellt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lIndex* \[ In\]
</dt> <dd>

Eine **System.Int32-Datei,** die den Index enthält, der die Wiedergabeliste identifiziert, die die Methode abrufen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die abgerufene Wiedergabeliste.

## <a name="remarks"></a>Hinweise

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

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

[**IWMPPlaylistArray-Schnittstelle (VB und C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





