---
title: MCI_WAVE_OPEN_PARMS-Struktur (Mciapi.h)
description: Die MCI \_ WAVE \_ OPEN \_ PARMS-Struktur enthält Informationen zum MCI \_ OPEN-Befehl für Waveform-Audio-Geräte.
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
ms.openlocfilehash: 470b00bc818fb184174f27a8ff281359788f235ec7e31b899b051dc90423426c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783784"
---
# <a name="mci_wave_open_parms-structure"></a>MCI \_ WAVE \_ OPEN \_ PARMS-Struktur

Die **MCI \_ WAVE OPEN \_ \_ PARMS-Struktur** enthält Informationen zum [**MCI \_ OPEN-Befehl**](mci-open.md) für Waveform-Audio-Geräte.

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

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Der Einzug wurde an die Anwendung zurückgegeben.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Name oder konstanter Bezeichner des Gerätetyps. (Der Name des Geräts wird in der Regel aus der Registrierung oder SYSTEM.INI Datei abgerufen.) Dieser Member kann einer der Werte sein, die unter [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Geräteelementname (in der Regel ein Pfad).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Optionaler Gerätealias.

</dd> <dt>

**dwBufferSeconds**
</dt> <dd>

Pufferlänge in Sekunden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

Sie können die [**MCI \_ OPEN \_ PARMS-Struktur**](mci-open-parms.md) anstelle von **MCI \_ WAVE OPEN \_ \_ PARMS** verwenden, wenn Sie die erweiterten Datenmember nicht verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ OPEN**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)
</dt> </dl>

 

