---
title: MCI_REALIZE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl "überprüfen" bewirkt, dass die Palette eines Grafik Geräts in einem Gerätekontext (DC) erkannt wird. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- MCI_REALIZE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339145"
---
# <a name="mci_realize-command"></a>Befehl "MCI- \_ Umsetzung"

Der MCI- \_ Befehl "überprüfen" bewirkt, dass die Palette eines Grafik Geräts in einem Gerätekontext (DC) erkannt wird. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
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

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lprealize*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Sie sollten diesen Befehl verwenden, wenn die Anwendung die [**WM- \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) -Nachricht empfängt.

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "Digitalvideo" verwendet:

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ realisiert \_ bkgd
</dt> <dd>

Erkennt die Palette als Hintergrund Palette.

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI \_ DGV-Integritäts \_ \_ Norm
</dt> <dd>

Erkennt die Palette normal. Dies ist die Standardoption.

</dd> </dl>

Für Digital Video-Geräte verweist der *lprealize* -Parameter auf eine **MCI-Struktur zum \_ realisieren von \_ para** Metern. Weitere Informationen finden Sie in den Kommentaren in der [**\_ generischen \_ MCI**](mci-generic-parms.md) -Struktur von Parametern.

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

 

