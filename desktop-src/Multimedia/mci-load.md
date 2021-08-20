---
title: MCI_LOAD Befehl (Mmsystem.h)
description: Der MCI \_ LOAD-Befehl lädt eine Datei. Digitale Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD Befehl Windows Multimedia
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
ms.openlocfilehash: e318e79bf24e51fec69f97a0dcb56395cb1a8917a31105deae062a865169b778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138538"
---
# <a name="mci_load-command"></a>MCI \_ LOAD-Befehl

Der MCI \_ LOAD-Befehl lädt eine Datei. Digitale Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder, für Digital Video-Geräte, MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

Zeiger auf eine [**MCI \_ LOAD \_ PARMS-Struktur.**](mci-load-parms.md) (Geräte mit zusätzlichen Parametern können diese Struktur durch eine gerätespezifische Struktur ersetzen. Bei Digitalvideogeräten verweist der **lpLoad-Parameter** auf eine [**MCI \_ DGV \_ LOAD \_ PARMS-Struktur.)**](/previous-versions//dd743391(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Das folgende zusätzliche Flag gilt für alle Geräte, die MCI \_ LOAD unterstützen:

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_ \_ MCI-LADEDATEI
</dt> <dd>

Der **lpfilename-Member** der durch *lpLoad* identifizierten Struktur enthält eine Adresse eines Puffers, der den Dateinamen enthält.

</dd> </dl>

Das folgende zusätzliche Flag wird mit dem **Überlagerungsgerätetyp** verwendet:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

Der **rc-Member** der von *lpLoad* identifizierten Struktur enthält ein gültiges Anzeigerechteck, das den Bereich des zu aktualisierenden Videopuffers identifiziert.

</dd> </dl>

Bei Videoüberlagerungsgeräten zeigt der *lpLoad-Parameter* auf eine [**MCI \_ OVLY \_ LOAD \_ PARMS-Struktur.**](mci-ovly-load-parms.md)

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

 

