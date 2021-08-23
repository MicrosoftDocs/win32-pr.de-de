---
title: MCI_UPDATE Befehl (Mmsystem.h)
description: Der MCI \_ UPDATE-Befehl aktualisiert das Anzeigerechteck. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE-Befehl Windows Multimedia
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
ms.openlocfilehash: e58333b108891a8bcd0e0548d4dcd0db2f2606d1259f0934f19b8f6804afab3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689680"
---
# <a name="mci_update-command"></a>MCI \_ UPDATE-Befehl

Der MCI \_ UPDATE-Befehl aktualisiert das Anzeigerechteck. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

**MCI \_ NOTIFY**, **MCI \_ WAIT** oder für Digitalvideogeräte **MCI \_ TEST**. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Zeiger auf eine [**MCI \_ GENERIC \_ PARMS-Struktur.**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen ersetzen diese Struktur möglicherweise durch eine gerätespezifische Struktur.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "digitalvideo" verwendet:

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI \_ DGV \_ UPDATE \_ HDC
</dt> <dd>

Der **hDC-Member** der durch *lpDest* identifizierten Struktur enthält ein gültiges Fenster des zu zeichnenden Domänencontrollers. Dieses Flag ist erforderlich.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

Der **rc-Member** der durch *lpUnfreeze* identifizierten Struktur enthält ein gültiges Anzeigerechteck. Das Rechteck gibt das Clippingrechteck relativ zum Clientrechteck an.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI \_ DGV \_ UPDATE \_ PAINT
</dt> <dd>

Eine Anwendung verwendet dieses Flag, wenn sie eine [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) empfängt, die für einen Anzeigedomänencontroller vorgesehen ist. Ein Framepuffergerät zeichnet in der Regel die Schlüsselfarbe. Wenn das Anzeigegerät über keinen Framepuffer verfügt, kann es den MCI UPDATE-Befehl ignorieren, wenn das \_ **MCI \_ DGV \_ UPDATE \_ PAINT-Flag** verwendet wird, da die Anzeige während des Wiedergabevorgang neu gepaint wird.

</dd> </dl>

Bei Digitalvideogeräten verweist *der lpDest-Parameter* auf eine [**MCI \_ DGV UPDATE \_ \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms)

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

 

