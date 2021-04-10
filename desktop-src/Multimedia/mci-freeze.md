---
title: MCI_FREEZE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Freeze-Befehl friert die Bewegung auf der Anzeige. Dieser Befehl wird von Digital Video, Video Overlay und VCR-Geräten erkannt.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- MCI_FREEZE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040302"
---
# <a name="mci_freeze-command"></a>MCI- \_ Freeze-Befehl

Der MCI- \_ Freeze-Befehl friert die Bewegung auf der Anzeige. Dieser Befehl wird von Digital Video, Video Overlay und VCR-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
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

<span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpfreeze*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit zusätzlichen Parametern können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags werden vom **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI \_ DGV- \_ Sperrung \_ bei
</dt> <dd>

Der **RC** -Member der durch *lpfreeze* identifizierten Struktur enthält ein gültiges Rechteck. Das Rechteck gibt einen Bereich innerhalb des Frame Puffers an, für den das Sperr Masken Bit für jedes Pixel aktiviert wird. Die angegebenen Pixel werden erst aktualisiert, wenn das Sperr Masken Bit ausgeschaltet ist. Wenn dieses Flag nicht angegeben wird, wird das Rechteck standardmäßig auf den gesamten Frame Puffer festgelegt. Dieses Flag wird nur unterstützt, wenn der [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl **true** zurückgibt, wenn das MCI \_ DGV- \_ Flag "getdevcaps-Lock" das \_ \_ Flag "

</dd> <dt>

<span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI \_ DGV- \_ Sperrung \_ außerhalb
</dt> <dd>

Der Bereich außerhalb der Region, der für das MCI DGV-Flag zum Fixieren bei festgelegt wurde, \_ \_ ist fixiert \_ .

</dd> </dl>

Bei Digital-Video-Geräten verweist der *lpfreeze* -Parameter auf eine [**MCI \_ DGV- \_ \_ sparstrukturstruktur**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .

Die folgenden zusätzlichen Flags werden vom **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI \_ VCR-Sperr \_ \_ Feld
</dt> <dd>

Fixiert nur einen Member des aktuellen Frames.

</dd> <dt>

<span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI \_ VCR- \_ Freeze- \_ Frame
</dt> <dd>

Fixiert beide Felder des aktuellen Frames.

</dd> <dt>

<span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI \_ VCR- \_ Freeze- \_ Eingabe
</dt> <dd>

Fixiert den aktuellen Frame auf dem Bildschirm (wird für die Aufzeichnung verwendet).

</dd> <dt>

<span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI \_ VCR- \_ Freeze- \_ Ausgabe
</dt> <dd>

Fixieren Sie den aktuellen Frame aus der VCR (verwendet mit Frame Erfassung).

</dd> </dl>

Bei VCR-Geräten verweist der *lpfreeze* -Parameter auf eine [**generische MCI \_ \_**](mci-generic-parms.md) -Parameter Struktur.

Das folgende zusätzliche Flag wird vom **überlagerungsgerätetyp** verwendet:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect
</dt> <dd>

Der **RC** -Member der durch *lpfreeze* identifizierten Struktur enthält ein gültiges Rechteck. Wenn dieses Flag nicht angegeben wird, fixiert der Gerätetreiber den gesamten Frame.

</dd> </dl>

Bei Video Überlagerungs Geräten zeigt der *lpfreeze* -Parameter auf eine MCI-Struktur mit [**\_ OVLY \_ Rect- \_ para**](mci-ovly-rect-parms.md) Metern.

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

 

