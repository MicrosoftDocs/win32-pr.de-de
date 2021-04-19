---
title: Iwmpmediacollection-Methode hinzufügen
description: Die Add-Methode fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu. | Iwmpmediacollection-Methode hinzufügen
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Hinzufügen von Methoden Fenster Media Player
- Add-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, Methode hinzufügen
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370509"
---
# <a name="iwmpmediacollectionadd-method"></a>Iwmpmediacollection:: Add-Methode

Die **Add** -Methode fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinurl* \[ in\]
</dt> <dd>

Eine **System. String** -URL, die den Speicherort des Medien Elements oder der Wiedergabeliste angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **WMPLib. iwmpmedia** -Schnittstelle für das hinzugefügte Element oder Wiedergabeliste.

## <a name="remarks"></a>Bemerkungen

Diese Methode lädt ein vorhandenes Medien Element oder eine vorhandene Wiedergabeliste in die Bibliothek, sofern ein Pfad angegeben ist. Diese Methode verschiebt oder ändert die Datei nicht. Bei dieser Methode tritt ein Fehler auf, wenn ein ungültiger lokaler Pfad vorliegt, die Medienelemente selbst jedoch nicht auf Gültigkeit überprüft werden, bevor Sie der Bibliothek hinzugefügt werden.

Diese Methode akzeptiert sowohl statische als auch automatische Wiedergabelisten Dateien. Die **iwmpplaylistcollection. importwiedergabe** -Methode kann auch verwendet werden, um der Bibliothek eine statische Wiedergabeliste hinzuzufügen.

Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden der Windows Media Player-Medien Auflistung drei Medienobjekte hinzugefügt. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
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

[**Iwmpmediacollection. Remove (VB und c#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. importwiedergabe (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





