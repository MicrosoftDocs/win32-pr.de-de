---
title: MCI_PASTE Befehl (Mmsystem.h)
description: Mit dem \_ MCI-Befehl EINFÜGEN werden Daten aus der Zwischenablage in eine Datei eingefügt. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdc7b27838236b09952a009f1cb8c7d60091afb6634bbd74fad213f013f6e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138231"
---
# <a name="mci_paste-command"></a>MCI \_ PASTE-Befehl

Mit dem \_ MCI-Befehl EINFÜGEN werden Daten aus der Zwischenablage in eine Datei eingefügt. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
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

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ PASTE \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags gelten für Digitalvideogeräte:

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI \_ DGV \_ PASTE \_ AT
</dt> <dd>

Ein Rechteck ist im **rc-Member** der -Struktur enthalten, die durch *lpPaste identifiziert wird.* Die ersten beiden Werte des Rechtecks geben den Punkt innerhalb des Frames an, um die Zwischenablageinformationen zu platzieren. Wenn Höhe und Breite des Rechtecks ungleich 0 (null) sind, wird der Inhalt der Zwischenablage auf diese Dimensionen skaliert, wenn sie in den Rahmen eingefügt werden. Wenn das Flag weggelassen wird, wird MCI \_ PASTE standardmäßig auf das gesamte Framerechteck festgelegt.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ PASTE \_ AUDIO \_ STREAM
</dt> <dd>

Eine Audiostreamnummer ist im **dwAudioStream-Member** der -Struktur enthalten, die durch *lpPaste identifiziert wird.* Wenn nur ein Audiostream in der Zwischenablage vorhanden ist, werden die Audiodaten in den angegebenen Stream eingefügt. Wenn mehr als ein Audiostream in der Zwischenablage vorhanden ist, gibt der Stream die Startnummer für die Streamsequenzen an. Wenn Sie dieses Flag verwenden und auch Video einfügen möchten, müssen Sie auch das MCI \_ DGV \_ PASTE VIDEO \_ \_ STREAM-Flag verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio- und Videostreams beginnend mit dem ersten Audio- und Videostream ein- und ausdingt. Jeder einfingierte Stream behält seine ursprüngliche Streamnummer bei.)

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI \_ DGV \_ PASTE \_ INSERT
</dt> <dd>

Zwischenablagedaten sollten an der durch das MCI TO-Flag angegebenen Position in den vorhandenen \_ Arbeitsbereich eingefügt werden. Alle vorhandenen Daten nach der Einfügemarke werden in den Arbeitsbereich verschoben, um Platz zu machen. Dies ist die Standardoption.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI \_ DGV \_ PASTE \_ OVERWRITE
</dt> <dd>

Zwischenablagedaten sollten daten ersetzen, die bereits im Arbeitsbereich vorhanden sind. Die ersetzten Arbeitsbereichsdaten folgen der Einfügemarke.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI \_ DGV \_ PASTE \_ VIDEO \_ STREAM
</dt> <dd>

Eine Videostreamnummer ist im **dwVideoStream-Member** der struktur enthalten, die durch *lpPaste identifiziert wird.* Wenn nur ein Videostream in der Zwischenablage vorhanden ist, werden die Videodaten in den angegebenen Stream eingefügt. Wenn mehr als ein Videostream in der Zwischenablage vorhanden ist, gibt der Stream die Startnummer für die Streamsequenzen an. Wenn Sie dieses Flag verwenden und auch Audio einfügen möchten, müssen Sie auch das MCI \_ DGV \_ PASTE AUDIO \_ \_ STREAM-Flag verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio- und Videostreams beginnend mit dem ersten Audio- und Videostream ein- und ausdingt. Jeder einfingierte Stream behält seine ursprüngliche Streamnummer bei.)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Ein Positionswert ist im **dwTo-Member** der -Struktur enthalten, die durch *lpPaste identifiziert wird.* Der Positionswert gibt die Position an, an der mit dem Einfingen von Daten in den Arbeitsbereich begonnen werden soll. Wenn dieses Flag weggelassen wird, wird die Position standardmäßig auf die aktuelle Position festgelegt.

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

 

