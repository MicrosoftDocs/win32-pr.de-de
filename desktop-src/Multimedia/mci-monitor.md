---
title: MCI_MONITOR Befehl (MMSYSTEM. h)
description: Der MCI- \_ Monitor-Befehl gibt die Präsentations Quelle an. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- MCI_MONITOR Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956776"
---
# <a name="mci_monitor-command"></a>MCI- \_ Monitor (Befehl)

Der MCI- \_ Monitor-Befehl gibt die Präsentations Quelle an. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
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

<span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpmonitor*
</dt> <dd>

Zeiger auf eine [**MCI- \_ DGV- \_ Monitor \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI- \_ DGV- \_ Monitor \_ Methode
</dt> <dd>

Eine-Konstante, die angibt, dass die Überwachungsmethode im **dwmethod** -Member der von *lpmonitor* identifizierten Struktur enthalten ist.

Wenn das Eingabe Kennzeichen für das MCI- \_ DGV- \_ Monitor \_ im **dwsource** -Member verwendet wird, wählt dies die Überwachungsmethode aus. In der Regel haben unterschiedliche Überwachungsmethoden andere Auswirkungen auf die Verwendung der Hardware. Die Standard Überwachungsmethode wird vom Gerät ausgewählt.

</dd> <dt>

<span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI- \_ DGV- \_ Monitor \_ Quelle
</dt> <dd>

Eine-Konstante, die angibt, dass die Monitor Quelle im **dwsource** -Member der von *lpmonitor* identifizierten Struktur enthalten ist.

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

 

