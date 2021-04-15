---
title: MCI_BREAK Befehl (MMSYSTEM. h)
description: Der MCI- \_ break-Befehl legt einen Break Key für ein MCI-Gerät fest. MCI unterstützt diesen Befehl direkt, anstatt ihn an das Gerät zu übergeben. Alle MCI-Anwendungen können diesen Befehl verwenden.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476239"
---
# <a name="mci_break-command"></a>MCI- \_ break-Befehl

Der MCI- \_ break-Befehl legt einen Break Key für ein MCI-Gerät fest. MCI unterstützt diesen Befehl direkt, anstatt ihn an das Gerät zu übergeben. Alle MCI-Anwendungen können diesen Befehl verwenden.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
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

MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und Video-Kassettenrecorder-Geräte (VCR), MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpbreak*
</dt> <dd>

Zeiger auf eine [**MCI-unter \_ Brechung \_**](mci-break-parms.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Sie müssen möglicherweise mehrmals die Unterbrechungs Taste drücken, um einen Warte Vorgang zu unterbrechen. Das Drücken der Pause-Taste, nachdem ein Geräte Wartezeit abgebrochen wurde, kann die Unterbrechung an eine Anwendung senden. Wenn für eine Anwendung eine Aktion definiert ist, die für den Code des virtuellen Schlüssels definiert ist, kann Sie versehentlich auf die Unterbrechung reagieren. Beispielsweise kann eine Anwendung, \_ die den VK-Abbruch für eine Zugriffstaste verwendet, auf die Standard Taste Strg + Pause reagieren, wenn Sie nach dem Abbrechen eines warte Vorgangs gedrückt wird.

Die folgenden zusätzlichen Flags gelten für alle Geräte:

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI- \_ break- \_ HWND
</dt> <dd>

Der **hwndbreak** -Member der durch *lpbreak* identifizierten Struktur enthält ein Fenster Handle, das das aktuelle Fenster sein muss, um die Unterbrechung für dieses MCI-Gerät zu aktivieren. Dies ist normalerweise das Hauptfenster der Anwendung. Wenn dieser nicht ausgelassen wird, überprüft MCI nicht das Fenster Handle des aktuellen Fensters.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI- \_ break- \_ Taste
</dt> <dd>

Der **nvirtkey** -Member der durch *lpbreak* identifizierten Struktur gibt den Code für den virtuellen Schlüssel an, der für die Pause-Taste verwendet wird. Standardmäßig weist MCI STRG + Unterbrechung als Break Key zu. Dieses Flag ist erforderlich, wenn die MCI-unter \_ Brechung \_ nicht angegeben ist.

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI-unter \_ Brechung \_
</dt> <dd>

Deaktiviert alle vorhandenen Break-Schlüssel für das Gerät.

</dd> </dl>

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

 

