---
title: AxWindowsMediaPlayer.URL (Eigenschaft)
description: Die URL-Eigenschaft ruft den Namen des medienelements ab, das wieder verwendet werden soll, oder legt diesen fest.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- URL-Windows Media Player
- URL-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , URL-Eigenschaft
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
ms.openlocfilehash: d953f2d85fc1fd83edcd37a491cb2f7cbabc3e3dfaf61e48feb1cd30e6d01934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123880"
---
# <a name="axwindowsmediaplayerurl-property"></a>AxWindowsMediaPlayer.URL (Eigenschaft)

Die URL-Eigenschaft ruft den Namen des medienelements ab, das wieder verwendet werden soll, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine System.String,die die URL des Medienelements ist.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann nur auf eine URL in einer Sicherheitszone festgelegt werden, die identisch oder weniger restriktiv als die Sicherheitszone des aufrufenden Programms oder der aufrufenden Webseite ist.

Anwendungen, die Medienelemente hinter einer Firewall öffnen, haben eine bessere Leistung, wenn die Adresse mithilfe des DNS-Namens (Domain Name Server) anstelle der IP-Adresse angegeben wird.

Rufen Sie diese Methode nicht aus dem Ereignishandlercode auf. Das **Aufrufen einer URL** von einem Ereignishandler kann zu unerwarteten Ergebnissen führen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel kann der Benutzer eine Mediendatei angeben, indem er einen Dateipfad in ein Textfeld ein gibt. Wenn auf eine Schaltfläche geklickt wird, wird die URL-Eigenschaft auf die angegebene Datei festgelegt, und die Datei wird abgespielt. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





