---
title: MCI_OVLY_WINDOW_PARMS-Struktur (mciapi. h)
description: Die Struktur der Fenster "MCI \_ OVLY \_ Window" \_ enthält Fenster Anzeigeinformationen für den MCI- \_ Fenster Befehl für Video Überlagerungs Geräte.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- MCI_OVLY_WINDOW_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949400"
---
# <a name="mci_ovly_window_parms-structure"></a>Struktur des MCI- \_ OVLY- \_ Fenster \_ Parametern

Die Struktur der Fenster " **MCI \_ OVLY \_ Window \_** " enthält Fenster Anzeigeinformationen für den [**MCI- \_ Fenster**](mci-window.md) Befehl für Video Überlagerungs Geräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**hWnd**
</dt> <dd>

Handle für Anzeige Fenster.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Fenster Anzeige Befehl.

</dd> <dt>

**lpstrautext**
</dt> <dd>

Fenster Beschriftung.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

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

[**MCI- \_ Fenster**](mci-window.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

