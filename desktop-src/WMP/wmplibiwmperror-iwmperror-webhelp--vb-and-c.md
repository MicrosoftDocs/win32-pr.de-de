---
title: Iwmperror WebHelp-Methode
description: Die WebHelp-Methode öffnet die Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen (Index null). | Iwmperror WebHelp-Methode
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- WebHelp-Methode (Windows Media Player)
- WebHelp-Methode, Windows Media Player, iwmperror-Schnittstelle
- Iwmperror Interface, Windows Media Player, WebHelp-Methode
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354772"
---
# <a name="iwmperrorwebhelp-method"></a>Iwmperror:: WebHelp-Methode

Die **WebHelp** -Methode öffnet die Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen (Index null).

## <a name="syntax"></a>Syntax


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Web-Hilfeseiten enthalten stets die neuesten und detailliertesten Informationen zu Windows Media Player-Fehlern. Diese Methode überträgt automatisch die anderen Informationen, die von der Webhilfe benötigt werden, z. b. die verwendete Betriebssystemversion.

Wenn Sie direkt auf die Web-Hilfeseiten zugreifen möchten, verwenden Sie die folgenden Links zu Fehlercode und Support Center:

-   [Windows Media Player-Fehler Code Informationen](https://support.microsoft.com/kb/886273)
-   [Windows Media Player-Lösungs Center](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Schaltfläche erstellt, mit der die Microsoft Windows Media Player-Webhilfe Seite im Browser gestartet wird. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmperror-Schnittstelle (VB und c#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





