---
title: MCI_CLOSE Befehl (MMSYSTEM. h)
description: Der Befehl zum \_ Schließen von MCI gibt den Zugriff auf ein Gerät oder eine Datei frei. Alle Geräte erkennen diesen Befehl.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- MCI_CLOSE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103443"
---
# <a name="mci_close-command"></a>Befehl zum Schließen von MCI \_

Der Befehl zum \_ Schließen von MCI gibt den Zugriff auf ein Gerät oder eine Datei frei. Alle Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI- \_ Benachrichtigung oder MCI- \_ Wartezeit. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpclose*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Sie können auch eine MCI-Struktur zum **\_ Schließen von \_ Parametern** verwenden. Weitere Informationen finden Sie in den Kommentaren zu **generischen MCI- \_ \_ Parametern**.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Anwendung beenden, ohne die geöffneten MCI-Geräte zu schließen, kann das Gerät nicht mehr zugänglich sein. Die Anwendung sollte jedes Gerät oder jede Datei explizit schließen, wenn Sie damit fertig ist. MCI entlädt das Gerät, wenn alle Instanzen des Geräts oder alle zugehörigen Dateien geschlossen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

