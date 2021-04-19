---
title: Iwmpplaylistarray-Element Methode
description: Die Item-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die die Wiedergabeliste am angegebenen Index darstellt.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, iwmpplaylistarray-Schnittstelle
- Iwmpplaylistarray Interface, Windows Media Player, Element-Methode
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
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354667"
---
# <a name="iwmpplaylistarrayitem-method"></a>Iwmpplaylistarray:: Item-Methode

Die **Item** -Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die die Wiedergabeliste am angegebenen Index darstellt.

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

*Lindex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der den Index enthält, der die Wiedergabeliste angibt, die die Methode abrufen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufene Wiedergabeliste.

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

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

[**Iwmpplaylistarray-Schnittstelle (VB und c#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





