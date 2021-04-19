---
title: Iwmpplaylistcollection (IsDeleted-Methode)
description: Die IsDeleted-Methode gibt einen Wert zurück, der angibt, ob sich die angegebene Wiedergabeliste im Ordner Gelöschte Elemente befindet.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- IsDeleted-Methode (Windows Media Player)
- IsDeleted-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle, Windows Media Player, IsDeleted-Methode
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
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367417"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>Iwmpplaylistcollection:: IsDeleted-Methode

Die **isDeleted** -Methode gibt einen Wert zurück, der angibt, ob sich die angegebene Wiedergabeliste im Ordner Gelöschte Elemente befindet.

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

*pitem* \[ in\]
</dt> <dd>

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgefragte Wiedergabeliste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Boolean** -Wert, der angibt, ob die Wiedergabeliste gelöscht wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection-Schnittstelle (VB und c#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





