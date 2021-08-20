---
title: MCI_MONITOR Befehl (Mmsystem.h)
description: Der MCI \_ MONITOR-Befehl gibt die Präsentationsquelle an. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- MCI_MONITOR-Befehl Windows Multimedia
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
ms.openlocfilehash: 6127a193feb16c6d2cdad21d2e99a062901be3ad37aab22fabfad172329ccc2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986310"
---
# <a name="mci_monitor-command"></a>MCI \_ MONITOR-Befehl

Der MCI \_ MONITOR-Befehl gibt die Präsentationsquelle an. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ MONITOR \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags gelten für Digitalvideogeräte:

<dl> <dt>

<span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI \_ DGV \_ \_ MONITOR-METHODE
</dt> <dd>

Eine Konstante, die die Überwachungsmethode angibt, ist im **dwMethod-Member** der struktur enthalten, die durch *lpMonitor identifiziert wird.*

Wenn das MCI \_ DGV \_ MONITOR \_ INPUT-Flag im **dwSource-Member** verwendet wird, wird die Überwachungsmethode ausgewählt. In der Regel haben verschiedene Überwachungsmethoden unterschiedliche Auswirkungen auf die Verwendung der Hardware. Die Standardüberwachungsmethode wird vom Gerät ausgewählt.

</dd> <dt>

<span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI \_ DGV \_ MONITOR \_ SOURCE
</dt> <dd>

Eine Konstante, die angibt, dass die Monitorquelle im **dwSource-Member** der struktur enthalten ist, die durch *lpMonitor identifiziert wird.*

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

 

