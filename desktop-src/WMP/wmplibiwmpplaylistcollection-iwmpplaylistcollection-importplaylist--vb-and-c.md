---
title: IWMPPlaylistCollection importPlaylist-Methode
description: Die importPlaylist-Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu. | IWMPPlaylistCollection importPlaylist-Methode
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- importPlaylist-Methode Windows Media Player
- importPlaylist-Methode Windows Media Player , IWMPPlaylistCollection-Schnittstelle
- IWMPPlaylistCollection-Schnittstelle Windows Media Player , importPlaylist-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ee4c231a045b39454908753dc197c95e26d85c711968f07ab27dbd859c29c6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122530"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>IWMPPlaylistCollection::importPlaylist-Methode

Die **importPlaylist-Methode** fügt der Bibliothek eine statische Wiedergabeliste hinzu.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pItem* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die Wiedergabeliste, die von dieser Methode hinzugefügt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPPlaylist-Schnittstelle** für die hinzugefügte Wiedergabeliste.

## <a name="remarks"></a>Hinweise

Wiedergabelisten, die keine Medienelemente enthalten, können der Bibliothek mit dieser Methode nicht hinzugefügt werden. Verwenden Sie die **newPlaylist-Methode,** um eine leere Wiedergabeliste in der Bibliothek zu erstellen. Anschließend können Sie die resultierende Wiedergabeliste mit Medienelementen füllen, indem **Sie IWMPPlaylist.appendItem** oder **IWMPPlaylist.insertItem** verwenden.

Wenn Sie diese Methode an eine automatische Wiedergabeliste übergeben, wird die Abfrage einmal ausgeführt, und das Ergebnis wird der Bibliothek als statische Wiedergabeliste hinzugefügt. Verwenden Sie **IWMPMediaCollection.add,** um der Bibliothek eine automatische Wiedergabeliste hinzuzufügen und ihr automatisches Verhalten beizubehalten. Weitere Informationen finden Sie unter [Statische und automatische Wiedergabelisten.](static-and-auto-playlists.md)

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player serie 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMediaCollection.add (VB und C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.appendItem (VB und C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.insertItem (VB und C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection-Schnittstelle (VB und C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.newPlaylist (VB und C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





