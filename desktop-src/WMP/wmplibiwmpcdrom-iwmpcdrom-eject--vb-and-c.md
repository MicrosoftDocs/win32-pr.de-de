---
title: IWMPC wie die eject-Methode
description: Die eject-Methode wirft die CD oder DVD vom Laufwerk aus. | IWMPC wie die eject-Methode
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- eject-Windows Media Player
- eject method Windows Media Player , IWMPCface interface
- IWMPCführungsschnittstelle Windows Media Player , eject-Methode
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00dbdf22d8eb0ba4073a1b74c25c0d610f3091477e5921dd0856fa835a9bccc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246760"
---
# <a name="iwmpcdromeject-method"></a>IWMPC datenträger::eject-Methode

Die **eject-Methode** wirft die CD oder DVD vom Laufwerk aus.

## <a name="syntax"></a>Syntax


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die Laufwerktür geöffnet ist, schließt diese Methode die Tür.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Tür des CD- oder DVD-Laufwerks mit dem Index 0 (null) als Reaktion auf das Click-Ereignis einer Schaltfläche mithilfe von **eject** geöffnet. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer.playState (VB und C#)**](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[**IWMPCwertschnittstelle (VB und C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





