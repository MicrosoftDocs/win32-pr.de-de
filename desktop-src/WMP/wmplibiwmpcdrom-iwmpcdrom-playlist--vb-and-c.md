---
title: Iwmpcdrom-Wiedergabelisten Eigenschaft
description: Die Wiedergabeliste Ruft eine iwmpwiedergabe-Schnittstelle ab, die die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk oder die Titel Einträge auf der Stamm Ebene einer DVD befinden.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Wiedergabelisten Eigenschaften Fenster Media Player
- Wiedergabelisten Eigenschaft, Windows Media Player, iwmpcdrom-Schnittstelle
- Iwmpcdrom-Schnittstelle, Windows Media Player, Wiedergabelisten Eigenschaft
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
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359629"
---
# <a name="iwmpcdromplaylist-property"></a>Iwmpcdrom::P laylist-Eigenschaft

Die **Wiedergabeliste** Ruft eine **iwmpwiedergabe** -Schnittstelle ab, die die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk oder die Titel Einträge auf der Stamm Ebene einer DVD befinden.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle.

## <a name="remarks"></a>Bemerkungen

In der Regel ist der DVD-basierte Inhalt in Titel gegliedert. Jeder Titel enthält ein oder mehrere Kapitel. Jede DVD wird unterschiedlich erstellt, sodass Titel und Kapitel für den Inhalts Autor verwendet werden.

Für eine DVD erhält diese Eigenschaft eine Wiedergabeliste, die als erstes Element eine **iwmpmedia** -Schnittstelle mit dem Namen "DVD" enthält. Diese Schnittstelle stellt das DVD-Medium dar. Die Wiedergabe des Elements führt dazu, dass die DVD von Anfang an wiedergegeben wird, wenn es sich um das erste Mal nach dem Einfügen einer neuen DVD handelt, oder die Wiedergabe wieder aufzunehmen, wenn die DVD mit der letzten angezeigten DVD identisch ist. Das Festlegen dieses Elements als Aktuelles Element während der Wiedergabe führt dazu, dass die DVD von Anfang an wiedergegeben wird.

Zusätzliche Elemente (die durch **iwmpmedia** -Schnittstellen dargestellt werden) in der Wiedergabeliste sind DVD-Titel, die durch eine Liste von in einer Liste dargestellten Wiedergabe Wenn Sie **iwmpcontrols.** Currency Item auf eine dieser geklickte Wiedergabelisten Elemente festlegen, legt Windows Media Player die geklickte Wiedergabeliste automatisch als aktuelle Wiedergabeliste fest, nachdem die Kapitel Wiedergabe begonnen hat. Sie können dann die Eigenschaften, Methoden und zugehörige Ereignisse der **iwmpwiedergabe** -Schnittstelle verwenden, um mit DVD-Kapiteln zu arbeiten, die auch Wiedergabelisten Elemente sind.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **Wiedergabe** Liste verwendet, um ein mehrzeilige Textfeld mit dem Namen MyText mit der Trackliste der AudioCD auszufüllen, die sich zurzeit auf dem ersten CD-Laufwerk befinden. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdrom-Schnittstelle (VB und c#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Currency Item (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





