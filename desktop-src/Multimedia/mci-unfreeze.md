---
title: MCI_UNFREEZE Befehl (MMSYSTEM. h)
description: Der MCI-Befehl zum Aufheben der Fixierung \_ stellt die Bewegung in einem Bereich des Video Puffers wieder her, der mit dem Befehl MCI Freeze eingefroren ist \_ . Dieser Befehl wird von digitalen Video-, VCR-und Video Überlagerungs Geräten erkannt.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105914"
---
# <a name="mci_unfreeze-command"></a>MCI-Befehl zum Einfrieren der Fixierung \_

Der MCI-Befehl zum Aufheben der Fixierung \_ stellt die Bewegung in einem Bereich des Video Puffers wieder her, der mit dem Befehl [MCI \_ Freeze](mci-freeze.md) eingefroren ist. Dieser Befehl wird von digitalen Video-, VCR-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
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

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpunfreeze*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Das folgende zusätzliche Flag wird mit dem **Digitalvideo** -Gerätetyp verwendet:

MCI- \_ DGV- \_ Rect

Der **RC** -Member der durch *lpunfreeze* identifizierten Struktur enthält ein gültiges Anzeige Rechteck. Das Rechteck gibt einen Bereich innerhalb des Frame Puffers an, dessen Pixel das Sperr Masken Bit deaktiviert werden soll. Rechteckige Bereiche werden wie für den Befehl [MCI \_ Put](mci-put.md) beschrieben angegeben. Wenn der Wert ausgelassen wird, wird das Rechteck standardmäßig auf den gesamten Frame Puffer eingestellt. Mithilfe einer Sequenz von Freeze-und Fixierung aufheben-Befehlen mit unterschiedlichen Rechtecke können beliebige Muster von Sperr Masken Bits beschrieben werden.

Für Digital Video-Geräte zeigt der *lpunfreeze* -Parameter auf eine **MCI \_ DGV \_ \_** -Struktur zum Aufheben der Fixierung von Parametern. Weitere Informationen finden Sie in den Kommentaren für die [**MCI-DGV-Struktur " \_ \_ Rect- \_ Parser**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) ".

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI \_ VCR- \_ einfrierende \_ Eingabe
</dt> <dd>

Entsperrung der Eingabe.

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI \_ VCR- \_ Ausgabe wird eingefroren \_
</dt> <dd>

Heben Sie die Fixierung der Ausgabe auf.

</dd> </dl>

Das folgende zusätzliche Flag wird mit dem **Überlagerungs** Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect
</dt> <dd>

Der **RC** -Member der durch *lpunfreeze* identifizierten Struktur enthält ein gültiges Anzeige Rechteck. Dies ist ein erforderlicher Parameter.

</dd> </dl>

Bei Video Überlagerungs Geräten zeigt der *lpunfreeze* -Parameter auf eine MCI-Struktur mit [**\_ OVLY \_ Rect- \_ para**](mci-ovly-rect-parms.md) Metern.

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

 

