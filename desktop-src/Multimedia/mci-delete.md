---
title: MCI_DELETE Befehl (Mmsystem.h)
description: Der MCI \_ DELETE-Befehl entfernt Daten aus der Datei. Digital-Video- und Waveform-Audio-Geräte erkennen diesen Befehl.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE Befehl Windows Multimedia
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
ms.openlocfilehash: ada80894f9260d0c37323d645694e10b0bcef92e52ebd670764bb9a0c436f837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784580"
---
# <a name="mci_delete-command"></a>MCI \_ DELETE-Befehl

Der MCI \_ DELETE-Befehl entfernt Daten aus der Datei. Digital-Video- und Waveform-Audio-Geräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder, für Digital Video-Geräte, MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*
</dt> <dd>

Zeiger auf eine [**GENERISCHE \_ MCI-PARMS-Struktur. \_**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden Flags gelten für den **Gerätetyp digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ DELETE \_ AT
</dt> <dd>

Ein Rechteck ist im **rc-Member** der durch *lpDelete* identifizierten Struktur enthalten. Das Rechteck gibt den Teil jedes zu löschenden Frames an. Wenn dieses Flag verwendet wird, wird der Rahmen im Arbeitsbereich beibehalten, und der durch das Rechteck angegebene Bereich wird schwarz. Wenn das Flag ausgelassen wird, wird standardmäßig der gesamte Frame von MCI DELETE verwendet, und der Frame wird \_ aus dem Arbeitsbereich entfernt.

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ DELETE \_ AUDIO \_ STREAM
</dt> <dd>

Eine Audiostreamnummer ist im **dwAudioStream-Member** der durch *lpDelete* identifizierten Struktur enthalten. Wenn Sie dieses Flag verwenden und auch Videos löschen möchten, müssen Sie auch das MCI \_ DGV \_ DELETE VIDEO \_ \_ STREAM-Flag verwenden. (Wenn kein Flag angegeben ist, werden Daten aus allen Audio- und Videostreams gelöscht.)

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI \_ DGV \_ DELETE \_ VIDEO \_ STREAM
</dt> <dd>

Eine Videostreamnummer ist im **dwVideoStream-Member** der durch *lpDelete identifizierten* Struktur enthalten. Wenn Sie dieses Flag verwenden und auch Audiodaten löschen möchten, müssen Sie auch das MCI \_ DGV \_ DELETE AUDIO \_ \_ STREAM-Flag verwenden. (Wenn kein Flag angegeben ist, werden Daten aus allen Audio- und Videostreams gelöscht.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Eine Startposition ist im **dwFrom-Member** der durch *lpDelete* identifizierten Struktur enthalten. Die den Positionswerten zugewiesenen Einheiten werden mit dem MCI \_ SET \_ TIME \_ FORMAT-Flag des [MCI \_ SET-Befehls](mci-set.md) angegeben.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Eine Endposition ist im **dwTo-Member** der durch *lpDelete* identifizierten Struktur enthalten. Die den Positionswerten zugewiesenen Einheiten werden mit dem MCI \_ SET \_ TIME \_ FORMAT-Flag von MCI \_ SET angegeben.

</dd> </dl>

Bei Digitalvideogeräten verweist der *lpDelete-Parameter* auf eine [**MCI \_ DGV \_ DELETE \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms)

Die folgenden Flags gelten für den **Waveaudio-Gerätetyp:**

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Eine Startposition ist im **dwFrom-Member** der durch *lpDelete* identifizierten Struktur enthalten. Die den Positionswerten zugewiesenen Einheiten werden mit dem MCI \_ SET \_ TIME \_ FORMAT-Flag von [MCI \_ SET](mci-set.md)angegeben.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Eine Endposition ist im **dwTo-Member** der durch *lpDelete* identifizierten Struktur enthalten. Die den Positionswerten zugewiesenen Einheiten werden mit dem MCI \_ SET \_ TIME \_ FORMAT-Flag von MCI \_ SET angegeben.

</dd> </dl>

Bei Waveform-Audiogeräten zeigt der *lpDelete-Parameter* auf eine [**MCI \_ WAVE DELETE \_ \_ PARMS-Struktur.**](mci-wave-delete-parms.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

