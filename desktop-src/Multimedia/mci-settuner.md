---
title: MCI_SETTUNER Befehl (Mmsystem.h)
description: Der Befehl MCI \_ SETTUNER legt den aktuellen Kanal auf dem Tuner fest. VCR-Geräte erkennen diesen Befehl.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- MCI_SETTUNER Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc0e4d812a89c8b7ca5a8e65b322e19dcb4f7d4e7e2ef8c49745ebb16e22af65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138106"
---
# <a name="mci_settuner-command"></a>MCI \_ SETTUNER-Befehl

Der Befehl MCI \_ SETTUNER legt den aktuellen Kanal auf dem Tuner fest. VCR-Geräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*
</dt> <dd>

Zeiger auf eine [**MCI \_ VCR \_ SETTUNER \_ PARMS-Struktur.**](mci-vcr-settuner-parms.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags gelten für VCR-Geräte:

<dl> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI \_ VCR \_ SETTUNER-KANAL \_
</dt> <dd>

Der **dwChannel-Member** der von *lpSetTuner* identifizierten Struktur enthält die neue Kanalnummer.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ DOWN
</dt> <dd>

Dekrementt den Tunerkanal.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ SEEK \_ DOWN
</dt> <dd>

Sucht in umgekehrter Richtung nach einem gültigen Kanal.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ SEEK \_ UP
</dt> <dd>

Sucht nach einem gültigen Kanal in Vorwärtsrichtung.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI \_ VCR \_ SETTUNER \_ CHANNEL \_ UP
</dt> <dd>

Erhöht den Tunerkanal.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI \_ VCR \_ SETTUNER \_ NUMBER
</dt> <dd>

Der **dwNumber-Member** der von *lpSetTuner* identifizierten Struktur gibt an, welcher logische Tuner mit diesem Befehl beeinflusst werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

