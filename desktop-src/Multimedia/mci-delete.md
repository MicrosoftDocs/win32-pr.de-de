---
title: MCI_DELETE Befehl (MMSYSTEM. h)
description: Mit dem MCI- \_ Befehl Delete werden Daten aus der Datei entfernt. Digital-Video-und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956777"
---
# <a name="mci_delete-command"></a>Befehl "MCI \_ Delete"

Mit dem MCI- \_ Befehl Delete werden Daten aus der Datei entfernt. Digital-Video-und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
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

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpdelete*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden Flags gelten für den **Digitalvideo** -Gerätetyp:

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ Delete \_ bei
</dt> <dd>

In den **RC** -Member der durch *lpdelete* identifizierten-Struktur ist ein Rechteck enthalten. Das Rechteck gibt den Teil jedes Frames an, der gelöscht werden soll. Wenn dieses Flag verwendet wird, wird der Frame im Arbeitsbereich aufbewahrt, und der durch das Rechteck angegebene Bereich wird schwarz. Wenn das Flag weggelassen wird, wird der \_ gesamte Frame vom MCI-Löschvorgang standardmäßig gelöscht und der Frame aus dem Arbeitsbereich entfernt.

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ , \_ \_ Audiostream löschen
</dt> <dd>

Im **dwaudiostream** -Member der von *lpdelete* identifizierten Struktur ist eine audiostreamnummer enthalten. Wenn Sie dieses Flag verwenden und Video auch löschen möchten, müssen Sie auch das Flag MCI \_ DGV- \_ \_ \_ Videostream löschen verwenden. (Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams gelöscht.)

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI \_ DGV \_ - \_ \_ Videostream löschen
</dt> <dd>

Im **dwvideostream** -Member der von *lpdelete* identifizierten Struktur ist eine Video Strom Nummer enthalten. Wenn Sie dieses Flag verwenden und auch Audiodaten löschen möchten, müssen Sie auch das Flag MCI \_ DGV \_ Delete \_ \_ Audiostream verwenden. (Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams gelöscht.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von
</dt> <dd>

Im **dwfrom** -Member der von *lpdelete* identifizierten-Struktur ist ein Start Speicherort enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Eine Endposition ist im **dwto** -Member der durch *lpdelete* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der MCI- \_ Menge angegeben.

</dd> </dl>

Bei Digital Video-Geräten verweist der *lpdelete* -Parameter auf eine [**MCI \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) -Struktur zum Löschen von Parametern.

Die folgenden Flags gelten für den **waveaudiogerätetyp** :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von
</dt> <dd>

Im **dwfrom** -Member der von *lpdelete* identifizierten-Struktur ist ein Start Speicherort enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der [MCI- \_ Menge](mci-set.md)angegeben.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Eine Endposition ist im **dwto** -Member der durch *lpdelete* identifizierten Struktur enthalten. Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der MCI- \_ Menge angegeben.

</dd> </dl>

Bei Waveform-Audiogeräten zeigt der *lpdelete* -Parameter auf eine [**MCI- \_ Wave \_ Delete \_**](mci-wave-delete-parms.md) -Parameter Struktur.

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

 

