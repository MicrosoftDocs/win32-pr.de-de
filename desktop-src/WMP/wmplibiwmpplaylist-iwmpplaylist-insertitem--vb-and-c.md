---
title: Iwmpwiedergabe InsertItem-Methode
description: Die InsertItem-Methode fügt ein Medien Element an einem angegebenen Speicherort in eine Wiedergabeliste ein.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- InsertItem-Methode, Windows-Media Player
- InsertItem-Methode, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, InsertItem-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365561"
---
# <a name="iwmpplaylistinsertitem-method"></a>Iwmpwiedergabe:: InsertItem-Methode

Die **InsertItem** -Methode fügt ein Medien Element an einem angegebenen Speicherort in eine Wiedergabeliste ein.

## <a name="syntax"></a>Syntax


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*Lindex* \[ in\]
</dt> <dd>

Ein **System. Int32** , bei dem es sich um den NULL basierten Index handelt, an dem das Medien Element in die Wiedergabeliste eingefügt wird.

</dd> <dt>

*piwmpmedia* \[ in\]
</dt> <dd>

Eine **WMPLib. iwmpmedia** -Schnittstelle, die das einzufügende Medien Element darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Für alle Medienelemente nach dem eingefügten Element werden die Indizes um eins erweitert.

Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. RemoveItem (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





