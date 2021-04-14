---
title: MCI_SIGNAL Befehl (MMSYSTEM. h)
description: Mit dem Befehl MCI- \_ Signal wird eine angegebene Position im Arbeitsbereich festgelegt. Dieser Befehl wird von Digital-Video-Geräten erkannt. MCIAVI unterstützt jeweils nur ein aktives Signal.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL Befehl Windows-Multimedia
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
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391821"
---
# <a name="mci_signal-command"></a>Befehl "MCI- \_ Signal"

Mit dem Befehl MCI- \_ Signal wird eine angegebene Position im Arbeitsbereich festgelegt. Dieser Befehl wird von Digital-Video-Geräten erkannt. MCIAVI unterstützt jeweils nur ein aktives Signal.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpsignal*
</dt> <dd>

Zeiger auf eine [**MCI- \_ DGV- \_ Signal \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Das Fenster, dessen Handle Sie im **dwcallback** -Member der [**MCI- \_ DGV- \_ Signal- \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) -Struktur angeben, empfängt die mm \_ mcisignal-Nachricht.

Die folgenden Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI \_ DGV- \_ Signal \_ bei
</dt> <dd>

Eine Signal Position ist im **dwposition** -Member der durch *lpsignal* identifizierten Struktur enthalten.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI- \_ DGV- \_ Signal \_ Abbruch
</dt> <dd>

Entfernt die Signal Position, die durch den dem MCI- \_ DGV- \_ Signal userval zugeordneten Wert angegeben wird \_ .

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI- \_ DGV- \_ Signal \_ alle
</dt> <dd>

Ein Signal Zeitraum-Wert ist im **dwperiod** -Member der durch *lpsignal* identifizierten Struktur enthalten.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI- \_ DGV- \_ Signal \_ Position
</dt> <dd>

Das Gerät sendet den Positionswert nicht mit dem vom Benutzer angegebenen Wert, sondern mit der Windows-Meldung.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV- \_ Signal \_ userval
</dt> <dd>

Ein Datenwert ist im **dwuserparamem** -Member der durch *lpsignal* identifizierten Struktur enthalten. Der Datenwert, der dieser Anforderung zugeordnet ist, wird mit der Windows-Meldung zurückgemeldet.

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

 

