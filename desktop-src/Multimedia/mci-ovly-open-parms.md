---
title: MCI_OVLY_OPEN_PARMS-Struktur (Mmsystem.h)
description: Die MCI \_ OVLY \_ OPEN \_ PARMS-Struktur enthält Informationen zum MCI \_ OPEN-Befehl für Videoüberlagerungsgeräte.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f13d0e9f8a7a4b9f5477459286bc56b9c98b1f9564e8432329681aeaef66d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138276"
---
# <a name="mci_ovly_open_parms-structure"></a>MCI \_ OVLY \_ OPEN \_ PARMS-Struktur

Die **MCI \_ OVLY \_ OPEN \_ PARMS-Struktur** enthält Informationen zum [**MCI \_ OPEN-Befehl**](mci-open.md) für Videoüberlagerungsgeräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Bezeichner, der an die Anwendung zurückgegeben wird.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Name oder konstanter Bezeichner des Gerätetyps. (Der Name des Geräts wird in der Regel aus der Registrierung oder SYSTEM.INI Datei abgerufen.) Wenn dieser Member eine Konstante ist, kann es sich um einen der in [MCI-Gerätetypen](mci-device-types.md)aufgeführten Werte handelt.

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Geräteelementname (in der Regel ein Pfad).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Optionaler Gerätealias.

</dd> <dt>

**dwStyle**
</dt> <dd>

Fensterformat.

</dd> <dt>

**hWndParent**
</dt> <dd>

Handle für übergeordnetes Fenster.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

Sie können die [**MCI \_ OPEN \_ PARMS-Struktur**](mci-open-parms.md) anstelle von **MCI \_ OVLY \_ OPEN \_ PARMS** verwenden, wenn Sie die erweiterten Datenmember nicht verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmsystem.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ OPEN**](mci-open.md)
</dt> <dt>

[**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

