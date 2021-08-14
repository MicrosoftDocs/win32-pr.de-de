---
title: MCI_MARK Befehl (Mmsystem.h)
description: Der MCI MARK-Befehl zeichnet Markierungen auf oder löscht Markierungen, die mit dem \_ MCI \_ SEEK-Befehl für schnelle Suchvorgänge verwendet werden können. VCR-Geräte erkennen diesen Befehl.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- MCI_MARK-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83cdb6c8c62fa19d66dc6042b6c8b16837f9dc4657060c0955098ed90e1c016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374995"
---
# <a name="mci_mark-command"></a>MCI \_ MARK-Befehl

Der MCI MARK-Befehl zeichnet Markierungen auf oder löscht Markierungen, die mit dem \_ [MCI \_ SEEK-Befehl](mci-seek.md) für schnelle Suchvorgänge verwendet werden können. VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
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

<span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*
</dt> <dd>

Zeiger auf eine [**MCI \_ GENERIC \_ PARMS-Struktur.**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen ersetzen diese Struktur möglicherweise durch eine gerätespezifische Struktur.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags gelten für VCR-Geräte:

<dl> <dt>

<span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI \_ VCR \_ MARK \_ ERASE
</dt> <dd>

Löscht eine Markierung an der aktuellen Position, sofern vorhanden.

</dd> <dt>

<span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI \_ VCR \_ MARK \_ WRITE
</dt> <dd>

Schreibt eine Markierung an der aktuellen Position.

</dd> </dl>

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

 

