---
title: MCI_BREAK Befehl (Mmsystem.h)
description: Der Befehl MCI \_ BREAK legt einen Halteschlüssel für ein MCI-Gerät fest. MCI unterstützt diesen Befehl direkt, anstatt ihn an das Gerät zu übergeben. Dieser Befehl kann von jeder MCI-Anwendung verwendet werden.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK-Befehl Windows Multimedia
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
ms.openlocfilehash: 07006ddfb38e1a57f6e08cb73d9b33021d139b9542245aec137e0969378140e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803969"
---
# <a name="mci_break-command"></a>Befehl "MCI \_ BREAK"

Der Befehl MCI \_ BREAK legt einen Halteschlüssel für ein MCI-Gerät fest. MCI unterstützt diesen Befehl direkt, anstatt ihn an das Gerät zu übergeben. Dieser Befehl kann von jeder MCI-Anwendung verwendet werden.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI NOTIFY, MCI WAIT oder für Geräte mit \_ \_ digital-video und video-cassette recorder (VCR) MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

Zeiger auf eine [**MCI \_ BREAK \_ PARMS-Struktur.**](mci-break-parms.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Möglicherweise müssen Sie die Haltetaste mehrmals drücken, um einen Wartevorgang zu unterbrechen. Wenn Sie die Haltetaste drücken, nachdem ein Gerätewartezeit abgebrochen wurde, kann die Unterbrechung an eine Anwendung gesendet werden. Wenn für eine Anwendung eine Aktion für den Code des virtuellen Schlüssels definiert ist, kann sie versehentlich auf die Unterbrechung reagieren. Beispielsweise kann eine Anwendung, die den VK CANCEL für eine Zugriffstaste verwendet, auf die Standardtaste STRG+BREAK reagieren, wenn sie nach dem Abbrechen eines Warte \_ vorgangs gedrückt wird.

Die folgenden zusätzlichen Flags gelten für alle Geräte:

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI \_ BREAK \_ HWND
</dt> <dd>

Das **hwndBreak-Member** der durch *lpBreak* identifizierten Struktur enthält ein Fensterhand handle, das das aktuelle Fenster sein muss, um die Erkennung von Unterbrechungen für dieses MCI-Gerät zu aktivieren. Dies ist normalerweise das Hauptfenster der Anwendung. Wenn nicht angegeben, überprüft MCI das Fensterhand handle des aktuellen Fensters nicht.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_ \_ MCI-BREAK-TASTE
</dt> <dd>

Der **nVirtKey-Member** der struktur, die durch *lpBreak* identifiziert wird, gibt den virtuellen Schlüsselcode an, der für den Break-Schlüssel verwendet wird. Standardmäßig weist MCI STRG+BREAK als Haltetaste zu. Dieses Flag ist erforderlich, wenn MCI \_ BREAK OFF nicht angegeben \_ ist.

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>\_MCI-ABBRUCH \_
</dt> <dd>

Deaktiviert alle vorhandenen Halteschlüssel für das angegebene Gerät.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

