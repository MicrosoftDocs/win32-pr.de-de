---
title: AxWindowsMediaPlayer. URL (Eigenschaft)
description: Die URL-Eigenschaft ruft den Namen des wieder zugebende Medien Elements ab oder legt ihn fest.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- URL-Eigenschaften Fenster Media Player
- URL-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, URL-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356007"
---
# <a name="axwindowsmediaplayerurl-property"></a>AxWindowsMediaPlayer. URL (Eigenschaft)

Die URL-Eigenschaft ruft den Namen des wieder zugebende Medien Elements ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein System. String-Wert, der die URL des Medien Elements ist.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nur auf eine URL in einer Sicherheitszone festgelegt werden, die identisch ist oder weniger restriktiv ist als die Sicherheitszone des aufrufenden Programms oder der Webseite.

Anwendungen, die Medienelemente hinter einer Firewall öffnen, haben eine bessere Leistung, wenn die Adresse anstelle der IP-Adresse mit dem DNS-Namen (Domain Nameserver) angegeben wird.

Diese Methode kann nicht aus dem Ereignishandlercode aufgerufen werden. Das Aufrufen von **URL** von einem Ereignishandler kann zu unerwarteten Ergebnissen führen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel kann der Benutzer eine Mediendatei angeben, indem er einen Dateipfad in ein Textfeld eingegeben hat. Wenn auf eine Schaltfläche geklickt wird, wird die URL-Eigenschaft auf die angegebene Datei festgelegt, und die Datei wird wiedergegeben. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





