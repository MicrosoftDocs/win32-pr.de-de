---
title: MCI_OVLY_LOAD_PARMS-Struktur (MMSYSTEM. h)
description: Die Struktur für den MCI- \_ OVLY- \_ Ladevorgang \_ enthält Informationen zum MCI \_ -Lade Befehl für Video Überlagerungs Geräte.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- MCI_OVLY_LOAD_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040078"
---
# <a name="mci_ovly_load_parms-structure"></a>Struktur von MCI- \_ OVLY- \_ Lade- \_ Parametern

Die Struktur für den **MCI- \_ OVLY- \_ Lade \_** Vorgang enthält Informationen zum [**MCI- \_ Lade**](mci-load.md) Befehl für Video Überlagerungs Geräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**lpFileName**
</dt> <dd>

Der Name der zu ladenden Datei.

</dd> <dt>

**RC**
</dt> <dd>

Identifiziert den Bereich des zu aktualisierenden Video Puffers. [Rect](/previous-versions//ms536136(v=vs.85)) -Strukturen werden in MCI anders behandelt als in anderen Teilen von Windows. in MCI enthält **RC. Right** die Breite des Rechtecks und **RC. Bottom** enthält die Höhe des Rechtecks.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI- \_ Auslastung**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[Rect](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

