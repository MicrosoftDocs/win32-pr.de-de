---
title: IWMPError webHelp-Methode
description: Die webHelp-Methode startet die Windows Media Player-Webhilfeseite, um weitere Informationen zum ersten Fehler in der Fehlerwarteschlange (Index 0) anzuzeigen. | IWMPError webHelp-Methode
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- webHelp-Windows Media Player
- webHelp-Windows Media Player , IWMPError-Schnittstelle
- IWMPError-Schnittstelle Windows Media Player , webHelp-Methode
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
ms.openlocfilehash: 50d4b404988e8b317ec7b090adcb96aac8e26a5a82590aa1138848dc797e3e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115823"
---
# <a name="iwmperrorwebhelp-method"></a>IWMPError::webHelp-Methode

Die **webHelp-Methode** startet die Windows Media Player-Webhilfeseite, um weitere Informationen zum ersten Fehler in der Fehlerwarteschlange (Index 0) anzuzeigen.

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

## <a name="remarks"></a>Hinweise

Die Webhilfeseiten enthalten immer die neuesten und ausführlichsten Informationen zu Windows Media Player Fehler. Diese Methode überträgt automatisch die anderen informationen, die von der Webhilfe benötigt werden, z. B. die verwendete Betriebssystemversion.

Verwenden Sie den folgenden Fehlercode und Die folgenden Links zum Supportcenter, um direkt auf die Webhilfeseiten zu zugreifen:

-   [Windows Media Player Fehlercodeinformationen](https://support.microsoft.com/kb/886273)
-   [Windows Media Player Solution Center](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Schaltfläche erstellt, die die Microsoft Windows Media Player-Webhilfeseite im Browser startet. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


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

[**IWMPError-Schnittstelle (VB und C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





