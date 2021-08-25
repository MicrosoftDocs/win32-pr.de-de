---
title: MCI_OVLY_WINDOW_PARMS -Struktur (Mciapi.h)
description: Die MCI OVLY WINDOW PARMS-Struktur enthält Fensteranzeigeinformationen für den \_ \_ \_ MCI \_ WINDOW-Befehl für Videoüberlagerungsgeräte.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- MCI_OVLY_WINDOW_PARMS-Struktur Windows Multimedia
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
ms.openlocfilehash: bd19580dacdc819f35bc36ed8f0070a5fc1b9fc4b745c78711c4fc312611e3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138284"
---
# <a name="mci_ovly_window_parms-structure"></a>MCI \_ OVLY \_ WINDOW \_ PARMS-Struktur

Die **MCI \_ OVLY \_ WINDOW \_ PARMS-Struktur** enthält Fensteranzeigeinformationen für den [**MCI \_ WINDOW-Befehl**](mci-window.md) für Videoüberlagerungsgeräte.

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

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**hWnd**
</dt> <dd>

Handle zum Anzeigen des Fensters.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Befehl "Fensteranzeige".

</dd> <dt>

**lpstrText**
</dt> <dd>

Fensterbeschriftung.

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

[**\_MCI-FENSTER**](mci-window.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

