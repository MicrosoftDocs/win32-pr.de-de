---
title: "' Iwmpmediacollection ' getbyattribute-Methode"
description: Die getbyattribute-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- getbyattribute-Methode, Windows-Media Player
- getbyattribute-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, getbyattribute-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370856"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>Iwmpmediacollection:: getbyattribute-Methode

Die **getbyattribute** -Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrattribute* \[ in\]
</dt> <dd>

Die **System. String** -Eigenschaft, die das angegebene Attribut ist.

</dd> <dt>

*bstrauvalue* \[ in\]
</dt> <dd>

Die **System. String** , die den angegebenen Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufenen Medienelemente.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann verwendet werden, um eine generische Abfrage für Medienelemente zu erstellen, die einem Wert für ein Attribut in der Bibliothek entsprechen. Dies ist nützlich für benutzerdefinierte Attribute. Wenn das Attribut nicht vorhanden ist, führt dies zu einem Fehler.

Mit dieser Methode können Sie alle Medienelemente eines bestimmten Typs abrufen. Verwenden Sie den Attributnamen " **mediaType** " und einen der folgenden Werte.



| Wert    | BESCHREIBUNG                                               |
|----------|-----------------------------------------------------------|
| Audio    | Musik und andere reine Audioelemente                          |
| andere    | Andere Elemente, wie z. b. eine. ASF-Datei oder die URL eines Streams. |
| Foto    | Foto Elemente. Erfordert Windows Media Player 10.            |
| Abspielen | Wiedergabelisten, die als Medienelemente dargestellt werden.                     |
| radio    | Radio Station-Elemente. Wird nicht von Windows Media Player 10 verwendet. |
| video    | Video Elemente.                                              |



 

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).

Es gibt zwei Möglichkeiten, wie Sie eine **iwmpmediacollection** -Schnittstelle abrufen können, und das Verhalten der **getbyattribute** -Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden. Wenn Sie die Schnittstelle abrufen, indem Sie [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)aufrufen, gibt die **getbyattribute** -Methode alle Medienelemente in der Bibliothek zurück. Wenn Sie jedoch die Schnittstelle abrufen, indem Sie [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)aufrufen, gibt die **getbyattribute** -Methode nur die Audioelemente in der Bibliothek zurück, die über das angegebene Attribut und den angegebenen Wert verfügen.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird **getbyattribute** verwendet, um den gesamten Inhalt der Bibliothek von der Künstlerin mit dem Namen "testode 48" wiederzugeben. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. GetAll (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





