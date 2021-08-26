---
title: IWMPError clearErrorQueue-Methode
description: Die clearErrorQueue-Methode löscht die Fehler aus der Fehlerwarteschlange. | IWMPError clearErrorQueue-Methode
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- clearErrorQueue-Methode Windows Media Player
- clearErrorQueue-Methode Windows Media Player , IWMPError-Schnittstelle
- IWMPError-Schnittstelle Windows Media Player , clearErrorQueue-Methode
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f75b4e4d2a0e80a3f55a38744758497abc71f5899498fee95ee3b3db752631c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000450"
---
# <a name="iwmperrorclearerrorqueue-method"></a>IWMPError::clearErrorQueue-Methode

Die **clearErrorQueue-Methode** löscht die Fehler aus der Fehlerwarteschlange.

## <a name="syntax"></a>Syntax


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um die Fehlerwarteschlange zu löschen, nachdem eine Reihe von Fehlern verarbeitet wurde.

Sie sollten **IWMPSettings.enableErrorDialogs** auf **FALSE** festlegen, wenn Sie benutzerdefinierte Fehlermeldungen anzeigen möchten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **clearErrorQueue** in einem Error-Ereignishandler verwendet, um die Fehlerwarteschlange zu leeren, nachdem alle Fehlerbeschreibungen angezeigt wurden. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPError-Schnittstelle (VB und C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB und C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





