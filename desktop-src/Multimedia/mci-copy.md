---
title: MCI_COPY Befehl (Mmsystem.h)
description: Der MCI \_ COPY-Befehl kopiert Daten in die Zwischenablage. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY Befehl Windows Multimedia
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
ms.openlocfilehash: 590acf61b352fa9abab00dfd49f3f54b166bfc340eaf12061e3d90b7a3025d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039290"
---
# <a name="mci_copy-command"></a>MCI \_ COPY-Befehl

Der MCI \_ COPY-Befehl kopiert Daten in die Zwischenablage. Digitalvideogeräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ COPY \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags gelten für Digitalvideogeräte:

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI \_ DGV \_ COPY \_ AT
</dt> <dd>

Ein Rechteck ist im **rc-Member** der durch *lpCopy* identifizierten Struktur enthalten. Das Rechteck gibt den Teil jedes zu kopierenden Frames an. Wenn das Flag ausgelassen wird, kopiert MCI \_ COPY den gesamten Frame.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI \_ DGV \_ COPY \_ AUDIO \_ STREAM
</dt> <dd>

Eine Audiostreamnummer ist im **dwAudioStream-Member** der struktur enthalten, die durch *lpCopy* identifiziert wird. Wenn Sie dieses Flag verwenden und auch Videos kopieren möchten, müssen Sie auch das MCI \_ DGV \_ COPY VIDEO \_ \_ STREAM-Flag verwenden. (Wenn kein Flag angegeben ist, werden Daten aus allen Audio- und Videostreams kopiert.)

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI \_ DGV \_ COPY \_ VIDEO \_ STREAM
</dt> <dd>

Eine Videostreamnummer ist im **dwVideoStream-Member** der durch *lpCopy* identifizierten Struktur enthalten. Wenn Sie dieses Flag verwenden und auch Audio kopieren möchten, müssen Sie auch das MCI \_ DGV \_ COPY AUDIO \_ \_ STREAM-Flag verwenden. (Wenn kein Flag angegeben ist, werden Daten aus allen Audio- und Videostreams kopiert.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ FROM
</dt> <dd>

Ein Startspeicherort ist im **dwFrom-Member** der durch *lpCopy* identifizierten Struktur enthalten. Die den Positionswerten zugewiesenen Einheiten werden mit dem MCI \_ SET \_ TIME \_ FORMAT-Flag des [MCI \_ SET-Befehls](mci-set.md) angegeben.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Eine Endposition ist im **dwTo-Member** der durch *lpCopy* identifizierten Struktur enthalten. Die den Positionswerten zugewiesenen Einheiten werden mit dem MCI \_ SET \_ TIME \_ FORMAT-Flag des MCI \_ SET-Befehls angegeben.

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

 

