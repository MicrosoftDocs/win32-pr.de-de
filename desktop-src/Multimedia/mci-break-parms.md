---
title: MCI_BREAK_PARMS-Struktur (Mciapi.h)
description: Die MCI \_ BREAK \_ PARMS-Struktur enthält Code für virtuelle Schlüssel und Fensterinformationen für den MCI \_ BREAK-Befehl.
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
ms.openlocfilehash: efaff8841e0e8ef0387535aa8d42723cf9477887511b7111f02a6ee0cb2b527b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039510"
---
# <a name="mci_break_parms-structure"></a>MCI \_ BREAK \_ PARMS-Struktur

Die **MCI \_ BREAK \_ PARMS-Struktur** enthält Code für virtuelle Schlüssel und Fensterinformationen für den [**MCI \_ BREAK-Befehl.**](mci-break.md)

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

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**nVirtKey**
</dt> <dd>

Virtueller Schlüsselcode für Halteschlüssel.

</dd> <dt>

**hwndBreak**
</dt> <dd>

Handle für das Fenster, das das aktuelle Fenster für die Unterbrechungserkennung sein muss.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen. Die folgenden Flags sind definiert:

MCI \_ BREAK \_ HWND

Überprüft das **hwndBreak-Element,** das das Fenster angibt, das den Fokus haben muss, um die Unterbrechungserkennung zu aktivieren.

\_MCI-BREAK \_ KEY

Überprüft das **nVirtKey-Element,** das den für den Halteschlüssel zu verwendenden Virtuellen Schlüsselcode angibt.

MCI \_ BREAK \_ OFF

Deaktiviert alle vorhandenen Halteschlüssel.

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

[**\_MCI-UNTERBRECHUNG**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

