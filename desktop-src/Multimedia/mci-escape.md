---
title: MCI_ESCAPE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl "Escape" sendet eine Zeichenfolge direkt an das Gerät. Videodisk-Geräte erkennen diesen Befehl.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- MCI_ESCAPE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339986"
---
# <a name="mci_escape-command"></a>MCI- \_ escapebefehl

Der MCI- \_ Befehl "Escape" sendet eine Zeichenfolge direkt an das Gerät. Videodisk-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
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

MCI- \_ Benachrichtigung oder MCI- \_ Wartezeit. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpescape*
</dt> <dd>

Zeiger auf eine [**MCI- \_ VD \_ \_**](mci-vd-escape-parms.md) -escapeparameterstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die mit der MCI-Escapesequenz gesendeten Daten \_ sind Geräte abhängig und werden normalerweise direkt an die dem Gerät zugeordnete Hardware übermittelt.

Das folgende zusätzliche Flag gilt für Videodisk-Geräte:

<dl> <dt>

<span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI VD-Escapesequenz \_ \_ \_
</dt> <dd>

Eine Befehls Zeichenfolge wird im **lpstrecommand** -Member der von *lpescape* identifizierten Struktur angegeben. Dieses Flag ist erforderlich.

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

 

