---
title: AxWindowsMediaPlayer. newwiedergabe-Methode
description: Die newwiedergabe-Methode gibt eine iwmpwiedergabe-Schnittstelle für eine neue Wiedergabeliste zurück.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- newwiedergabe-Methode, Windows-Media Player
- newwiedergabe-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, newwiedergabe-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370205"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a>AxWindowsMediaPlayer. newwiedergabe-Methode

Die newwiedergabe-Methode gibt eine iwmpwiedergabe-Schnittstelle für eine neue Wiedergabeliste zurück.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrName* 
</dt> <dd>

Die **System. String** -Wert, der der Name der neuen Wiedergabeliste ist.

</dd> <dt>

*bstrURL* 
</dt> <dd>

Die **System. String** -URL, die die URL der Windows Media Metadatei-Wiedergabeliste ist, die zum Initialisieren der neuen Wiedergabeliste verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine WMPLib. iwmpwiedergabe-Schnittstelle, die die neu erstellte Wiedergabeliste darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn der *bstrinurl* -Parameter eine NULL-Zeichenfolge oder eine Zeichenfolge der Länge 0 ("") ist, erstellt diese Methode eine leere **Wiedergabeliste**. Wenn der *bstrinname* -Parameter eine Zeichenfolge der Länge 0 ("") ist, wendet diese Methode den aktuellen metadateinamen an.

Die neue Wiedergabeliste, die mit dieser Methode erstellt wurde, wird nicht der Bibliothek hinzugefügt. Um der Bibliothek eine neue Wiedergabeliste hinzuzufügen, verwenden Sie iwmpplaylistcollection. **importwiedergabe Liste** oder iwmpplaylistcollection. **newwiedergabe**. Alle führenden oder nachfolgenden Leerzeichen im Wiedergabelisten Namen werden automatisch entfernt, wenn Sie der Bibliothek hinzugefügt werden.

Da die Bibliothek mehrere Wiedergabelisten mit dem gleichen Namen zulässt, sollten Sie überprüfen, ob eine Wiedergabeliste mit einem bestimmten Namen vorhanden ist, bevor Sie einen neuen hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. importwiedergabe (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. newwiedergabe (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





