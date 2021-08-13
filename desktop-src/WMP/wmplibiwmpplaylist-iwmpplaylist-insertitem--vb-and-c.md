---
title: IWMPPlaylist insertItem-Methode
description: Die insertItem-Methode fügt ein Medienelement an einer angegebenen Position in einer Wiedergabeliste ein.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- insertItem-Methode Windows Media Player
- insertItem-Methode Windows Media Player , IWMPPlaylist-Schnittstelle
- IWMPPlaylist-Schnittstelle Windows Media Player , insertItem-Methode
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
ms.openlocfilehash: 10717c0891443aaa663b748be6a0cb57e04e58b96beb91db6b02b2f6a4b5b621
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464930"
---
# <a name="iwmpplaylistinsertitem-method"></a>IWMPPlaylist::insertItem-Methode

Die **insertItem-Methode** fügt ein Medienelement an einer angegebenen Position in einer Wiedergabeliste ein.

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

*lIndex* \[ In\]
</dt> <dd>

Eine **System.Int32-Datei,** bei der es sich um den nullbasierten Index handelt, an dem das Medienelement in die Wiedergabeliste eingefügt wird.

</dd> <dt>

*pIWMPMedia* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPMedia-Schnittstelle,** die das einzufügende Medienelement darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Für alle Medienelemente nach dem eingefügten Element werden die Indizes um eins erhöht.

Vor dem Aufrufen dieser Methode benötigen Sie Vollzugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.removeItem (VB und C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





