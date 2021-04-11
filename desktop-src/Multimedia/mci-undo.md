---
title: MCI_UNDO Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Undo kehrt mit dem letzten erfolgreichen MCI-Befehl, dem MCI- \_ Kopiervorgang, dem \_ MCI DELETE-Befehl oder dem \_ MCI-Befehl " \_ Einfügen" zurück. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 1593457a-e680-4732-a89e-00f4eff7605a
keywords:
- MCI_UNDO Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_UNDO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d099d95159afee8d91acb77eb64e8e80bee5425d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040221"
---
# <a name="mci_undo-command"></a>Befehl "MCI \_ Rückgängig"

Der Befehl MCI \_ Undo kehrt mit dem letzten erfolgreichen [MCI- \_ ](mci-cut.md)Befehl, dem MCI- [ \_ Kopier](mci-copy.md)Vorgang, dem [MCI \_ Delete](mci-delete.md)-Befehl oder dem MCI-Befehl " [ \_ Einfügen](mci-paste.md) " zurück. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNDO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUndo
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

<span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpundo*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

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

 

