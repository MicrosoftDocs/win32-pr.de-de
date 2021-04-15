---
title: MCI_BREAK_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI \_ \_ -break-Parser enthält Code-und Fenster Informationen des virtuellen Schlüssels für den MCI- \_ break-Befehl.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- MCI_BREAK_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517630"
---
# <a name="mci_break_parms-structure"></a>Struktur der MCI- \_ break- \_ Parametern

Die Struktur der **MCI- \_ break- \_ Parser** enthält Code-und Fenster Informationen des virtuellen Schlüssels für den [**MCI- \_ break**](mci-break.md) -Befehl.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**nvirtkey**
</dt> <dd>

Code des virtuellen Schlüssels für die Pause-Taste.

</dd> <dt>

**hwndbreak**
</dt> <dd>

Handle für das Fenster, das das aktuelle Fenster für die unterschieterkennung sein muss.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen. Die folgenden Flags sind definiert:

MCI- \_ break- \_ HWND

Überprüft das **hwndbreak** -Element und gibt das Fenster an, das den Fokus haben muss, um die Unterbrechung zu aktivieren.

MCI- \_ break- \_ Taste

Überprüft den **nvirtkey** -Member, der den Code für den virtuellen Schlüssel angibt, der für die Break Key-Taste verwendet werden soll.

MCI-unter \_ Brechung \_

Deaktiviert alle vorhandenen Break-Schlüssel.

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

[**MCI-unter \_ Brechung**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

