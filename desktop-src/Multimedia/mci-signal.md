---
title: MCI_SIGNAL Befehl (Mmsystem.h)
description: Der Befehl MCI \_ SIGNAL legt eine angegebene Position im Arbeitsbereich fest. Digitalvideogeräte erkennen diesen Befehl. MCIAVI unterstützt nur ein aktives Signal gleichzeitig.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda7585ad63415f888f5971397df2b27c23710864ea21a8ed5e6ebce1a7c66f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689840"
---
# <a name="mci_signal-command"></a>MCI \_ SIGNAL-Befehl

Der Befehl MCI \_ SIGNAL legt eine angegebene Position im Arbeitsbereich fest. Digitalvideogeräte erkennen diesen Befehl. MCIAVI unterstützt nur ein aktives Signal gleichzeitig.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
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

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ SIGNAL \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Das Fenster, dessen Handle Sie im **dwCallback-Member** der [**MCI \_ DGV \_ SIGNAL \_ PARMS-Struktur**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) angeben, empfängt die MM \_ MCISIGNAL-Nachricht.

Die folgenden Flags gelten für Digitalvideogeräte:

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI \_ DGV \_ SIGNAL \_ AT
</dt> <dd>

Eine Signalposition ist im **dwPosition-Member** der -Struktur enthalten, die durch *lpSignal identifiziert wird.*

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI \_ DGV \_ SIGNAL \_ CANCEL
</dt> <dd>

Entfernt die Signalposition, die durch den Wert angegeben wird, der MCI \_ DGV \_ SIGNAL \_ USERVAL zugeordnet ist.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI \_ DGV \_ SIGNAL \_ EVERY
</dt> <dd>

Ein Signalzeitraumwert ist im **dwPeriod-Member** der struktur enthalten, die durch *lpSignal identifiziert wird.*

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI \_ DGV \_ SIGNAL \_ POSITION
</dt> <dd>

Das Gerät sendet den Positionswert mit der Windows anstelle des vom Benutzer angegebenen Werts.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV \_ SIGNAL \_ USERVAL
</dt> <dd>

Ein Datenwert ist im **dwUserParm-Member** der struktur enthalten, die durch *lpSignal identifiziert wird.* Der datenwert, der dieser Anforderung zugeordnet ist, wird mit der Windows gemeldet.

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

 

