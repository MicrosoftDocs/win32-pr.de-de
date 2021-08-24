---
title: IWMPPlaylist removeItem-Methode
description: Die removeItem-Methode entfernt das angegebene Medienelement aus der Wiedergabeliste.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- removeItem-Methode Windows Media Player
- removeItem-Methode Windows Media Player , IWMPPlaylist-Schnittstelle
- IWMPPlaylist-Schnittstelle Windows Media Player , removeItem-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ea9250cc7e368699a916b4c87f419fc5b0b66001a4d7ca12afd5587a0adda7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246429"
---
# <a name="iwmpplaylistremoveitem-method"></a>IWMPPlaylist::removeItem-Methode

Die **removeItem-Methode** entfernt das angegebene Medienelement aus der Wiedergabeliste.

## <a name="syntax"></a>Syntax


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pIWMPMedia* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPMedia-Schnittstelle,** die das Medienelement darstellt, das aus der Wiedergabeliste entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn das entfernte Element die aktuell wiedergegebene Spur ist, wird die Wiedergabe beendet, und das nächste Element in der Wiedergabeliste wird zum aktuellen Element.

Wenn kein nächstes Element vorhanden ist, wird das vorherige Element verwendet. Wenn keine anderen Elemente vorhanden sind, gibt die **AxWindowsMediaPlayer.currentMedia-Eigenschaft** **NULL** zurück.

Vor dem Aufrufen dieser Methode benötigen Sie Vollzugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player Serie 9 oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB und C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.insertItem (VB und C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.Item (VB und C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





