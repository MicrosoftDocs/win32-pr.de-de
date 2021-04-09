---
title: MCI_COPY Befehl (MMSYSTEM. h)
description: Der MCI- \_ Kopier Befehl kopiert Daten in die Zwischenablage. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956528"
---
# <a name="mci_copy-command"></a>MCI- \_ Kopier Befehl

Der MCI- \_ Kopier Befehl kopiert Daten in die Zwischenablage. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
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

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpcopy*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ - \_ kopierparamemestruktur**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI \_ DGV- \_ Kopie \_ bei
</dt> <dd>

Ein Rechteck ist im **RC** -Member der durch *lpcopy* identifizierten Struktur enthalten. Das Rechteck gibt den Teil jedes Frames an, der kopiert werden soll. Wenn das Flag weggelassen wird, kopiert MCI \_ Copy den gesamten Frame.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI \_ DGV \_ \_ - \_ Audiodatenstrom kopieren
</dt> <dd>

Im **dwaudiostream** -Member der durch *lpcopy* identifizierten Struktur ist eine audiostreamnummer enthalten. Wenn Sie dieses Flag verwenden und Videos auch kopieren möchten, müssen Sie auch das Flag MCI \_ DGV- \_ \_ \_ Videostream kopieren verwenden. (Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams kopiert.)

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI \_ DGV \_ - \_ \_ Videostream zum Kopieren
</dt> <dd>

Im **dwvideostream** -Member der durch *lpcopy* identifizierten Struktur ist eine Video Strom Nummer enthalten. Wenn Sie dieses Flag verwenden und auch Audiodaten kopieren möchten, müssen Sie auch das Flag MCI \_ DGV \_ \_ - \_ Audiodatenstrom verwenden. (Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams kopiert.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von
</dt> <dd>

Ein Start Speicherort ist im **dwfrom** -Member der durch *lpcopy* identifizierten-Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Eine Endposition ist im **dwto** -Member der durch *lpcopy* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls MCI \_ Set angegeben.

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

 

