---
title: IWMPPlaylistCollection isDeleted-Methode
description: Die isDeleted-Methode gibt einen Wert zurück, der angibt, ob sich die angegebene Wiedergabeliste im Ordner gelöschte Elemente befindet.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- isDeleted-Methode Windows Media Player
- isDeleted-Methode Windows Media Player , IWMPPlaylistCollection-Schnittstelle
- IWMPPlaylistCollection-Schnittstelle Windows Media Player , isDeleted-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c332a524b334933d587929cdd0e5b5fa61bc15d9110260af8af8e472d7c05fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568477"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>IWMPPlaylistCollection::isDeleted-Methode

Die **isDeleted-Methode** gibt einen Wert zurück, der angibt, ob sich die angegebene Wiedergabeliste im Ordner gelöschte Elemente befindet.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pItem* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die abgefragte Wiedergabeliste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Boolean,** der angibt, ob die Wiedergabeliste gelöscht wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player serie 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection-Schnittstelle (VB und C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





