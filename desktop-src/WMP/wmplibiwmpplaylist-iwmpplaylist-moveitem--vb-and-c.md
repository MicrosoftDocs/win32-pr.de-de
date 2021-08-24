---
title: IWMPPlaylist moveItem-Methode
description: Die moveItem-Methode ändert die Position eines Medienelements in der Wiedergabeliste.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- moveItem-Methode Windows Media Player
- moveItem-Methode Windows Media Player , IWMPPlaylist-Schnittstelle
- IWMPPlaylist-Schnittstelle Windows Media Player , moveItem-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f2c4f2aa3d4478a114e405b1b40816fc1697c2c291c272aabc68db3813766d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760660"
---
# <a name="iwmpplaylistmoveitem-method"></a>IWMPPlaylist::moveItem-Methode

Die **moveItem-Methode** ändert die Position eines Medienelements in der Wiedergabeliste.

## <a name="syntax"></a>Syntax


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lIndexOld* \[ In\]
</dt> <dd>

Ein **System.Int32,** das der ursprüngliche Index ist.

</dd> <dt>

*lIndexNeu* \[ In\]
</dt> <dd>

Eine **System.Int32,die** der neue Index ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Für alle Elemente nach dem eingefügten Element werden die Indexnummern um eins erhöht.

Vor dem Aufrufen dieser Methode benötigen Sie Vollzugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





