---
title: MCI_STEP Befehl (MMSYSTEM. h)
description: Der MCI- \_ Schritt Befehl führt den Player um einen oder mehrere Frames. Videodisk-Geräte Digital Video, VCR und CAV-Format erkennen diesen Befehl.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- MCI_STEP Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102846"
---
# <a name="mci_step-command"></a>Befehl "MCI- \_ Schritt"

Der MCI- \_ Schritt Befehl führt den Player um einen oder mehrere Frames. Videodisk-Geräte Digital Video, VCR und CAV-Format erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
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

<span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpstep*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Dieser Befehl unterstützt Geräte, die " **true** " zurückgeben, für das MCI \_ getdevcaps- \_ Video Kennzeichen \_ des Befehls [MCI \_ getdevcaps](mci-getdevcaps.md) .

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI- \_ DGV- \_ Schritt \_ Rahmen
</dt> <dd>

Der **dwframes** -Member der durch *lpstep* identifizierten-Struktur gibt die Anzahl der Frames an, die vor dem Anzeigen eines anderen Bilds fortgesetzt werden sollen.

</dd> <dt>

<span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI- \_ DGV- \_ Schritt \_ umkehren
</dt> <dd>

Schritte in umgekehrter Reihenfolge.

</dd> </dl>

Bei Digital-Video-Geräten verweist der *lpstep* -Parameter auf eine [**MCI- \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) -Struktur.

Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI- \_ VCR- \_ Schritt \_ Rahmen
</dt> <dd>

Der **dwframes** -Member der durch *lpstep* identifizierten-Struktur gibt die Anzahl der Frames an, die vor dem Anzeigen eines anderen Bilds fortgesetzt werden sollen.

</dd> <dt>

<span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI- \_ VCR- \_ Schritt \_ umkehren
</dt> <dd>

Schritte in umgekehrter Reihenfolge.

</dd> </dl>

Bei VCR-Geräten verweist der *lpstep* -Parameter auf eine [**MCI- \_ VCR- \_ Schritt \_**](mci-vcr-step-parms.md) -Parameter-Struktur.

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp " **Videodisk** " verwendet:

<dl> <dt>

<span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI- \_ VD- \_ Schritt- \_ Frames
</dt> <dd>

Der **dwframes** -Member der-Struktur, die von *lpstep* identifiziert wird, gibt die Anzahl der zu schrifenden Rahmen an.

</dd> <dt>

<span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI- \_ VD- \_ Schritt \_ umkehren
</dt> <dd>

Schritte in umgekehrter Reihenfolge.

</dd> </dl>

Bei Videodisk-Geräten verweist der *lpstep* -Parameter auf eine MCI-Schritt-für- [**\_ \_ Schritt \_**](mci-vd-step-parms.md) -Struktur.

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

 

