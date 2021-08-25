---
title: Hinzufügen einer IWMPMediaCollection-Methode
description: Die add-Methode fügt der Bibliothek ein neues Medienelement oder eine neue Wiedergabeliste hinzu. | Hinzufügen einer IWMPMediaCollection-Methode
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- add method Windows Media Player
- Add-Methode Windows Media Player , IWMPMediaCollection-Schnittstelle
- IWMPMediaCollection-Schnittstelle Windows Media Player , Methode hinzufügen
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
ms.openlocfilehash: 778850da4094d8ac745018b115248de9008d15339b7ffee75de177cf957d3fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861162"
---
# <a name="iwmpmediacollectionadd-method"></a>IWMPMediaCollection::add-Methode

Die **add-Methode** fügt der Bibliothek ein neues Medienelement oder eine neue Wiedergabeliste hinzu.

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

*bstrURL* \[ In\]
</dt> <dd>

Eine **System.String,die** die URL ist, die den Speicherort des Medienelements oder der Wiedergabeliste angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **WMPLib.IWMPMedia-Schnittstelle** für das hinzugefügte Element oder die Wiedergabeliste.

## <a name="remarks"></a>Hinweise

Diese Methode lädt ein vorhandenes Medienelement oder eine vorhandene Wiedergabeliste unter Berücksichtigung eines Pfads in die Bibliothek. Mit dieser Methode wird die Datei nicht verschoben oder geändert. Diese Methode schlägt fehl, wenn ein ungültiger lokaler Pfad angegeben wird, Medienelemente selbst jedoch nicht auf Gültigkeit überprüft werden, bevor sie der Bibliothek hinzugefügt werden.

Diese Methode akzeptiert sowohl statische als auch automatische Wiedergabelistendateien. Die **IWMPPlaylistCollection.importPlaylist-Methode** kann auch verwendet werden, um der Bibliothek eine statische Wiedergabeliste hinzuzufügen.

Vor dem Aufrufen dieser Methode benötigen Sie Vollzugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden der Windows Media Player Medienauflistung drei Medienobjekte hinzugefügt. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.remove (VB und C#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.importPlaylist (VB und C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





