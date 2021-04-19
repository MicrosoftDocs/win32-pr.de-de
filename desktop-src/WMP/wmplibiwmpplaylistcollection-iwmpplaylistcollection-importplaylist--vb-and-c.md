---
title: Iwmpplaylistcollection importwiedergabe-Methode
description: Die importwiedergabe-Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu. | Iwmpplaylistcollection importwiedergabe-Methode
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- importwiedergabe-Methode, Windows-Media Player
- importwiedergabe-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle Windows Media Player, importwiedergabe Methode
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
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350779"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>Iwmpplaylistcollection:: importwiedergabe-Methode

Die **importwiedergabe** -Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu.

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

*pitem* \[ in\]
</dt> <dd>

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die Wiedergabeliste, die von dieser Methode hinzugefügt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die hinzugefügte Wiedergabeliste.

## <a name="remarks"></a>Bemerkungen

Wiedergabelisten, die keine Medienelemente enthalten, können der Bibliothek nicht mithilfe dieser Methode hinzugefügt werden. Verwenden Sie die **newwiedergabe** -Methode, um eine leere Wiedergabeliste in der Bibliothek zu erstellen. Anschließend können Sie die resultierende Wiedergabeliste mit den Medien Elementen füllen, indem Sie **iwmpwiedergabe. appendItem** oder **iwmpwiedergabe. InsertItem** verwenden.

Wenn Sie diese Methode an eine automatische Wiedergabeliste übergeben, wird die Abfrage einmal ausgeführt, und das Ergebnis wird der Bibliothek als statische Wiedergabeliste hinzugefügt. Wenn Sie der Bibliothek eine automatische Wiedergabeliste hinzufügen und das automatische Verhalten beibehalten möchten, verwenden Sie **iwmpmediacollection. Add**. Weitere Informationen finden Sie unter [statische und automatische Wiedergabelisten](static-and-auto-playlists.md).

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmediacollection. Add (VB und c#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. appendItem (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. InsertItem (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection-Schnittstelle (VB und c#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. newwiedergabe (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





