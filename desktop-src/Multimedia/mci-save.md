---
title: MCI_SAVE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl Save speichert die aktuelle Datei.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- MCI_SAVE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475693"
---
# <a name="mci_save-command"></a>Befehl zum Speichern von MCI \_

Der MCI- \_ Befehl Save speichert die aktuelle Datei. Geräte, die Dateien ändern, sollten die ursprüngliche Kopie erst zerstören, wenn Sie die Speicher Nachricht erhalten. Video-Overlay-und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI-und mciseq-Treiber Sie nicht.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
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

MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpsave*
</dt> <dd>

Zeiger auf eine [**MCI-Struktur zum \_ Speichern von \_ Parametern**](mci-save-parms.md) . (Geräte mit zusätzlichen Parametern können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Dieser Befehl wird von Geräten unterstützt, die " **true** " zurückgeben, wenn Sie den [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl mit dem MCI \_ getdevcaps- \_ Flag " \_ Save Save" aufrufen.

Das folgende zusätzliche Flag gilt für alle Geräte, die [MCI- \_ Speicher](/windows)unterstützen:

<dl> <dt>

<span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI \_ - \_ Datei speichern
</dt> <dd>

Der **lpFileName** -Member der durch *lpsave* identifizierten Struktur enthält eine Adresse eines Puffers, der den Ziel Dateinamen enthält.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI- \_ DGV- \_ Rect
</dt> <dd>

Der **RC** -Member der durch *lpsave* identifizierten Struktur enthält ein gültiges Rechteck. Das Rechteck gibt einen Bereich des Frame Puffers an, der in der angegebenen Datei gespeichert wird. Das erste Koordinaten paar gibt die linke obere Ecke des Rechtecks an. Das zweite paar gibt die Breite und Höhe an. Digital Video-Geräte müssen den [MCI- \_ Erfassungs](mci-capture.md) Befehl verwenden, um den Inhalt des Frame Puffers aufzuzeichnen. (Video Überlagerungs Geräte sollten auch MCI \_ verwenden Erfassen.) Dieses Flag ist aus Gründen der Kompatibilität mit dem vorhandenen MCI-Video-Overlay-Befehlssatz.

</dd> <dt>

<span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI- \_ DGV- \_ Speicher \_ Abbruch
</dt> <dd>

Beendet einen aktuell ausgeführten Speichervorgang. Dies muss das einzige Flag sein, das vorhanden ist.

</dd> <dt>

<span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ Save \_ keepreserve
</dt> <dd>

Nicht verwendeter Speicherplatz aus dem ursprünglichen [MCI- \_ Reserve](mci-reserve.md) Befehl wird nicht aufgehoben.

</dd> </dl>

Für Digital Video-Geräte zeigt der *lpsave* -Parameter auf eine [**MCI \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) -Struktur zum Speichern von Parametern.

Das folgende zusätzliche Flag wird mit dem **Überlagerungs** Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect
</dt> <dd>

Der **RC** -Member der durch *lpsave* identifizierten Struktur enthält ein gültiges Anzeige Rechteck, das den Bereich des zu speichernden Video Puffers angibt.

</dd> </dl>

Bei Video Überlagerungs Geräten verweist der *lpsave* -Parameter auf eine [**MCI- \_ OVLY- \_ Speicher \_**](/previous-versions//dd743447(v=vs.85)) Struktur.

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

 

