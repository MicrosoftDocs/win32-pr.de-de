---
title: MCI_LOAD Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Load lädt eine Datei. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949403"
---
# <a name="mci_load-command"></a>Befehl "MCI \_ Load"

Der Befehl MCI \_ Load lädt eine Datei. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
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

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpload*
</dt> <dd>

Zeiger auf eine Struktur des [**MCI- \_ Lade- \_ Parametern**](mci-load-parms.md) . (Geräte mit zusätzlichen Parametern können diese Struktur durch eine gerätespezifische Struktur ersetzen. Für Digital Video-Geräte zeigt der **lpload** -Parameter auf eine [**MCI \_ DGV \_ \_**](/previous-versions//dd743391(v=vs.85)) -Struktur zum Laden von Daten.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Das folgende zusätzliche Flag gilt für alle Geräte, die die MCI-Auslastung unterstützen \_ :

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI- \_ Auslastungs \_ Datei
</dt> <dd>

Der **lpFileName** -Member der durch *lpload* identifizierten Struktur enthält eine Adresse eines Puffers, der den Dateinamen enthält.

</dd> </dl>

Das folgende zusätzliche Flag wird mit dem **Überlagerungs** Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect
</dt> <dd>

Der **RC** -Member der durch *lpload* identifizierten Struktur enthält ein gültiges Anzeige Rechteck, das den Bereich des zu aktualisierenden Video Puffers angibt.

</dd> </dl>

Bei Video Überlagerungs Geräten verweist der *lpload* -Parameter auf eine MCI-Struktur für das [**\_ OVLY- \_ Laden von \_ para**](mci-ovly-load-parms.md) Metern.

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

 

