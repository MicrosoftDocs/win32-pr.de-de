---
title: MCI_CAPTURE Befehl (MMSYSTEM. h)
description: Der MCI \_ -Aufzeichnungs Befehl erfasst den Inhalt des Frame Puffers und speichert ihn in einer angegebenen Datei. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956779"
---
# <a name="mci_capture-command"></a>MCI- \_ Aufzeichnungs Befehl

Der MCI \_ -Aufzeichnungs Befehl erfasst den Inhalt des Frame Puffers und speichert ihn in einer angegebenen Datei. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
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

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpcapture*
</dt> <dd>

Zeiger auf eine [**MCI- \_ DGV- \_ Erfassungs \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI- \_ DGV- \_ Erfassung \_ als
</dt> <dd>

Der **lpstrinfilename** -Member der durch *lpcapture* identifizierten Struktur enthält die Adresse eines Puffers, der den Zielpfad und den Dateinamen angibt. (Dieses Flag ist erforderlich.)

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI \_ DGV- \_ Erfassung \_ unter
</dt> <dd>

Der **RC** -Member der durch *lpcapture* identifizierten Struktur enthält ein gültiges Rechteck. Das Rechteck gibt den rechteckigen Bereich innerhalb des Frame Puffers an, der abgeschnitten und auf dem Datenträger gespeichert wird. Wenn der Wert nicht angegeben wird, wird der zugeschnittenen Bereich standardmäßig auf das Rechteck festgelegt oder standardmäßig auf einen vorherigen [MCI \_ Put](mci-put.md) -Befehl festgelegt, der den Quellbereich für diese Instanz des Gerätetreibers angibt.

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

 

