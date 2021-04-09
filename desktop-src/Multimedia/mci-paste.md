---
title: MCI_PASTE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl zum Einfügen fügt Daten aus der Zwischenablage in eine Datei ein. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE Befehl Windows-Multimedia
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
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739825"
---
# <a name="mci_paste-command"></a>MCI- \_ Befehl "Einfügen"

Der MCI- \_ Befehl zum Einfügen fügt Daten aus der Zwischenablage in eine Datei ein. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lppaste*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) -Struktur zum Einfügen von Parametern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI \_ DGV \_ Einfügen \_ bei
</dt> <dd>

In den **RC** -Member der durch *lppaste* identifizierten Struktur ist ein Rechteck enthalten. Die ersten beiden Werte des Rechtecks geben den Punkt im Frame an, an dem die Zwischenablage Informationen platziert werden sollen. Wenn die Höhe und Breite des Rechtecks ungleich NULL sind, werden die Inhalte der Zwischenablage auf diese Dimensionen skaliert, wenn Sie im Frame eingefügt werden. Wenn das-Flag weggelassen wird, wird der MCI-Wert \_ standardmäßig in das gesamte Frame Rechteck eingefügt.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ \_ - \_ Audiodatenstrom einfügen
</dt> <dd>

Im **dwaudiostream** -Member der durch *lppaste* identifizierten Struktur ist eine audiostreamnummer enthalten. Wenn nur ein Audiostream in der Zwischenablage vorhanden ist, werden die Audiodaten in den vorgesehenen Stream eingefügt. Wenn mehr als ein Audiostream in der Zwischenablage vorhanden ist, gibt der Stream die Startnummer für die Datenstrom Sequenzen an. Wenn Sie dieses Flag verwenden und Video einfügen möchten, müssen Sie auch das Flag MCI \_ DGV- \_ Videodaten \_ Strom einfügen verwenden \_ . (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams beginnend mit dem ersten Audiostream und Videostream eingefügt. Jeder eingefügte Stream behält seine ursprüngliche Datenstrom Nummer bei.)

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>Einfügen von MCI \_ DGV \_ Einfügen \_
</dt> <dd>

Zwischenablage Daten sollten in den vorhandenen Arbeitsbereich an der Position eingefügt werden, die durch das zu flagende MCI angegeben wird \_ . Alle vorhandenen Daten nach der Einfügemarke werden in den Arbeitsbereich verschoben, um Platz zu schaffen. Dies ist die Standardoption.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI- \_ DGV- \_ Einfüge \_ Überschreibung
</dt> <dd>

Zwischenablage Daten sollten die bereits im Arbeitsbereich vorhandenen Daten ersetzen. Die Arbeitsbereichs Daten werden nach der Einfügemarke ersetzt.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI \_ DGV \_ - \_ Video Daten \_ Strom einfügen
</dt> <dd>

Im **dwvideostream** -Member der durch *lppaste* identifizierten Struktur ist eine Video Strom Nummer enthalten. Wenn nur ein Videostream in der Zwischenablage vorhanden ist, werden die Videodaten in den vorgesehenen Stream eingefügt. Wenn mehr als ein Videostream in der Zwischenablage vorhanden ist, gibt der Stream die Startnummer für die Datenstrom Sequenzen an. Wenn Sie dieses Flag verwenden und auch Audiodaten einfügen möchten, müssen Sie auch das Flag MCI \_ DGV \_ \_ -Audiodatenstrom einfügen verwenden \_ . (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams beginnend mit dem ersten Audiostream und Videostream eingefügt. Jeder eingefügte Stream behält seine ursprüngliche Datenstrom Nummer bei.)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu
</dt> <dd>

Ein Positionswert ist im **dwto** -Member der durch *lppaste* identifizierten Struktur enthalten. Der Positionswert gibt die Position an, an der mit dem Einfügen von Daten in den Arbeitsbereich begonnen wird. Wenn dieses Flag weggelassen wird, wird die Position standardmäßig auf die aktuelle Position eingestellt.

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

 

