---
title: MCI_RESTORE Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Restore kopiert eine Bitmap aus einer Datei in den Frame Puffer. Dieser Befehl wird von Digital-Video-Geräten erkannt. Dieser Befehl führt die umgekehrte Aktion des MCI- \_ Erfassungs Befehls aus.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- MCI_RESTORE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742809"
---
# <a name="mci_restore-command"></a>MCI- \_ Restore-Befehl

Der Befehl MCI \_ Restore kopiert eine Bitmap aus einer Datei in den Frame Puffer. Dieser Befehl wird von Digital-Video-Geräten erkannt. Dieser Befehl führt die umgekehrte Aktion des [MCI- \_ Erfassungs](mci-capture.md) Befehls aus.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
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

<span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lprestore*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ Restore \_ -paramemstruktur**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die-Implementierung kann eine Vielzahl von Bildformaten erkennen, aber eine Windows-geräteunabhängige Bitmap (DIB) wird immer akzeptiert.

Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI \_ DGV- \_ Wiederherstellung \_ von
</dt> <dd>

Der **lpstrinfilename** -Member der durch *lprestore* identifizierten Struktur enthält eine Adresse eines Puffers, der den Quell Dateinamen enthält. Der Dateiname ist erforderlich.

</dd> <dt>

<span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI \_ DGV- \_ Wiederherstellung \_ unter
</dt> <dd>

Der **RC** -Member der durch *lprestore* identifizierten Struktur enthält ein gültiges Rechteck. Das Rechteck gibt einen Bereich des Frame Puffers relativ zum Ursprung an. Das erste Koordinaten paar gibt die linke obere Ecke des Rechtecks an. Das zweite paar gibt die Breite und Höhe an. Wenn dieses Flag nicht angegeben wird, wird das Bild in die linke obere Ecke des Frame Puffers kopiert.

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

 

