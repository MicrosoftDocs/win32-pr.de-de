---
title: IWMPC playlist-Eigenschaft
description: Die Playlist-Eigenschaft ruft eine IWMPPlaylist-Schnittstelle ab, die die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk befinden, oder die Titeleinträge auf Stammebene für eine DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Playlist-Eigenschaft Windows Media Player
- Playlist-Eigenschaft Windows Media Player , IWMPCnutzeroberfläche
- IWMPCaku-Schnittstelle Windows Media Player , Playlist-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ff17e3716f01308957b3f5f247759fb3f18f639f7b279a8f00d7f6f9e2189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116607"
---
# <a name="iwmpcdromplaylist-property"></a>IWMPClay::P laylist-Eigenschaft

Die **Playlist-Eigenschaft** ruft eine **IWMPPlaylist-Schnittstelle** ab, die die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk befinden, oder die Titeleinträge auf Stammebene für eine DVD.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib.IWMPPlaylist-Schnittstelle.**

## <a name="remarks"></a>Hinweise

In der Regel dvdbasierte Inhalte, die in Titeln organisiert sind. Jeder Titel enthält mindestens ein Kapitel. Jede DVD wird anders erstellt, sodass die Verwendung von Titeln und Kapiteln dem Inhaltsautor obliegt.

Bei einer DVD ruft diese Eigenschaft eine Wiedergabeliste ab, die als erstes Element eine **IWMPMedia-Schnittstelle** namens "DVD" enthält. Diese Schnittstelle stellt die DVD-Medien dar. Die Wiedergabe des Elements führt dazu, dass die DVD von Anfang an wiedergegeben wird, wenn es sich um die erste Wiedergabe nach dem Einfügen einer neuen DVD handelt, oder die Wiedergabe wird wieder aufgenommen, wenn die DVD mit der letzten angezeigten DVD identisch ist. Wenn dieses Element während der Wiedergabe als aktuelles Element festgelegt wird, wird die DVD von Anfang an wiedergegeben.

Zusätzliche Elemente (dargestellt durch **IWMPMedia-Schnittstellen)** in der Wiedergabeliste sind DVD-Titel, die durch geschachtelte Wiedergabelisten dargestellt werden. Wenn Sie **IWMPControls.currentItem** auf eines dieser geschachtelten Wiedergabelistenelemente festlegen, legt Windows Media Player die geschachtelte Wiedergabeliste automatisch als aktuelle Wiedergabeliste fest, nachdem die Kapitelwiedergabe beginnt. Anschließend können Sie die **IWMPPlaylist-Schnittstelleneigenschaften,** -Methoden und zugehörigen Ereignisse verwenden, um mit DVD-Kapiteln zu arbeiten, bei denen es sich ebenfalls um Wiedergabelistenelemente handelt.

Um den Wert dieser Eigenschaft abzurufen, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **playlist** verwendet, um ein mehrzeiliges Textfeld namens myText mit der Titelliste der Audio-CD auszufüllen, die sich derzeit auf dem ersten CD-Laufwerk befindet. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPCaku-Schnittstelle (VB und C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentItem (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





