---
title: MCI_OPEN_PARMS -Struktur (Mciapi.h)
description: Die MCI \_ OPEN \_ PARMS-Struktur enthält Informationen für den MCI \_ OPEN-Befehl.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- MCI_OPEN_PARMS-Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80d01f41db904cea583f83aa446e718d1067e99e4d8bac3a3c6791ef5696f83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138305"
---
# <a name="mci_open_parms-structure"></a>MCI \_ OPEN \_ PARMS-Struktur

Die **MCI \_ OPEN \_ PARMS-Struktur** enthält Informationen für den [**MCI \_ OPEN-Befehl.**](mci-open.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Bezeichner, der an die Anwendung zurückgegeben wird.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Name oder konstanter Bezeichner des Gerätetyps. (Der Name des Geräts wird in der Regel aus der Registrierung oder SYSTEM.INI erhalten.) Wenn es sich bei diesem Member um eine Konstante handelt, kann es sich um einen der unter [MCI-Gerätetypen aufgeführten Werte handelt.](mci-device-types.md)

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Device-Element (häufig ein Pfad).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Optionaler Gerätealias.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

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
</dt> </dl>

 

