---
title: MCI_WAVE_OPEN_PARMS-Struktur (mciapi. h)
description: Die \_ Struktur von MCI Wave \_ Open \_ -Parametern enthält Informationen für den MCI \_ -Befehl Open für Waveform-Audiogeräte.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- MCI_WAVE_OPEN_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344690"
---
# <a name="mci_wave_open_parms-structure"></a>MCI \_ Wave \_ Open- \_ paramemstruktur

Die Struktur von **MCI \_ Wave \_ Open- \_ Parametern** enthält Informationen für den [**MCI-Befehl \_ Open**](mci-open.md) für Waveform-Audiogeräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**WDE viceid**
</dt> <dd>

Der INDENTIFIER wurde an die Anwendung zurückgegeben.

</dd> <dt>

**lpstraude vicetype**
</dt> <dd>

Der Name oder Konstantenbezeichner des Gerätetyps. (Der Name des Geräts wird in der Regel aus der Registrierung oder SYSTEM.INI Datei abgerufen.) Dieser Member kann einer der Werte sein, die in den [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.

</dd> <dt>

**lpstrelementname**
</dt> <dd>

Der Name des Geräte Elements (in der Regel ein Pfad).

</dd> <dt>

**lpstraualias**
</dt> <dd>

Optionaler Gerätealias.

</dd> <dt>

**dwbufferseconds**
</dt> <dd>

Pufferlänge in Sekunden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

Wenn Sie die erweiterten Datenmember nicht verwenden, können Sie die [**MCI-Struktur \_ Open- \_ Parser**](mci-open-parms.md) anstelle von **MCI \_ Wave Open- \_ \_ para** Metern verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ geöffnet**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**geöffnete MCI- \_ \_ Parser**](mci-open-parms.md)
</dt> </dl>

 

