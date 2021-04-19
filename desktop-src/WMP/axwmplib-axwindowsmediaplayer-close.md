---
title: AxWindowsMediaPlayer. Close-Methode
description: Die Close-Methode schließt die aktuelle digitale Mediendatei, beendet die Wiedergabe in Windows Media Player und gibt Windows Media Player-Ressourcen frei.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- Schließen von Methoden Fenstern Media Player
- Close-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, Close-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366980"
---
# <a name="axwindowsmediaplayerclose-method"></a>AxWindowsMediaPlayer. Close-Methode

Die Close-Methode schließt die aktuelle digitale Mediendatei, beendet die Wiedergabe in Windows Media Player und gibt Windows Media Player-Ressourcen frei.

## <a name="syntax"></a>Syntax


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode schließt die aktuelle digitale Mediendatei, nicht Windows Media Player selbst.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Schaltfläche erstellt, bei der die Wiedergabe in Windows Media Player beendet wird und die verwendeten Ressourcen freigegeben werden. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

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

 

 





