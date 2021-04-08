---
title: MCI_CUT Befehl (MMSYSTEM. h)
description: Mit dem MCI \_ -Befehl "Ausschneiden" werden Daten aus der Datei entfernt und in die Zwischenablage kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- MCI_CUT Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956778"
---
# <a name="mci_cut-command"></a>MCI- \_ Befehl zum Ausschneiden

Mit dem MCI \_ -Befehl "Ausschneiden" werden Daten aus der Datei entfernt und in die Zwischenablage kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
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

<span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpcut*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV- \_ Ausschneide- \_ Parametern**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI \_ DGV- \_ Ausschneiden \_ um
</dt> <dd>

Ein Rechteck ist im **RC** -Member der-Struktur enthalten, die von *lpcut* identifiziert wird. Das Rechteck gibt den Teil jedes Frames an, der abgeschnitten werden soll. Wenn das Flag weggelassen wird, schneidet die MCI- \_ Ausschneide den gesamten Frame ab.

</dd> <dt>

<span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI \_ DGV \_ \_ -Audiodatenstrom Ausschneiden \_
</dt> <dd>

Eine audiostreamnummer ist im **dwaudiostream** -Member der durch *lpcut* identifizierten Struktur enthalten. Wenn Sie dieses Flag verwenden und auch Video ausschneiden möchten, müssen Sie auch das Flag MCI \_ DGV \_ - \_ Videodaten Strom verwenden \_ . (Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams ausgeschnitten.)

</dd> <dt>

<span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI \_ DGV- \_ Ausschneide \_ Video Daten \_ Strom
</dt> <dd>

Im **dwvideostream** -Member der durch *lpcut* identifizierten Struktur ist eine Video Strom Nummer enthalten. Wenn Sie dieses Flag verwenden und auch das Audioelement ausschneiden möchten, müssen Sie auch das Flag MCI \_ DGV \_ \_ - \_ Audiodatenstrom verwenden. (Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams ausgeschnitten.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von
</dt> <dd>

Ein Start Speicherort ist im **dwfrom** -Member der durch *lpcut* identifizierten-Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Eine Endposition ist im **dwto** -Member der durch *lpcut* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der MCI- \_ Menge angegeben.

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

 

