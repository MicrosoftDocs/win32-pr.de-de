---
title: MCI_UPDATE Befehl (MMSYSTEM. h)
description: Der Befehl "MCI- \_ Update" aktualisiert das Anzeige Rechteck. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105909"
---
# <a name="mci_update-command"></a>Befehl "MCI- \_ Update"

Der Befehl "MCI- \_ Update" aktualisiert das Anzeige Rechteck. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

**MCI \_ Benachrichtigen**, **MCI- \_ Wartezeit** oder, für Digital-Video-Geräte, **MCI- \_ Test**. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpdest*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "Digitalvideo" verwendet:

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI- \_ DGV- \_ Update- \_ hdc
</dt> <dd>

Das **hdc** -Mitglied der durch *lpdest* identifizierten Struktur enthält ein gültiges Fenster des Domänen Controllers, das gezeichnet werden soll. Dieses Flag ist erforderlich.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI- \_ DGV- \_ Rect
</dt> <dd>

Der **RC** -Member der durch *lpunfreeze* identifizierten Struktur enthält ein gültiges Anzeige Rechteck. Das Rechteck gibt das Clippingrechteck relativ zum Client Rechteck an.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI \_ DGV- \_ Update \_ Paint
</dt> <dd>

Eine Anwendung verwendet dieses Flag, wenn Sie eine [**WM \_**](/windows/desktop/gdi/wm-paint) -Zeichnungs Nachricht empfängt, die für einen Anzeige-DC vorgesehen ist. Ein Frame Puffer Gerät zeichnet in der Regel die Schlüsselfarbe. Wenn das Anzeigegerät nicht über einen Frame Puffer verfügt, wird möglicherweise der Befehl MCI-Update ignoriert, \_ Wenn das **MCI DGV-Flag zum \_ \_ Zeichnen von \_ Paint** verwendet wird, da die Anzeige während des Wiedergabe Vorgangs neu gezeichnet wird.

</dd> </dl>

Für Digital Video-Geräte verweist der *lpdest* -Parameter auf eine [**MCI- \_ DGV- \_ Update \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) -Parameter-Struktur.

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

 

