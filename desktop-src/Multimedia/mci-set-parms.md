---
title: MCI_SET_PARMS-Struktur (Mciapi.h)
description: Die MCI \_ SET \_ PARMS-Struktur enthält Informationen für den MCI \_ SET-Befehl.
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- MCI_SET_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c223534410b7e5a0543683c354728e0d5093f38ad0a2582a047a2a5362faae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986212"
---
# <a name="mci_set_parms-structure"></a>MCI \_ SET \_ PARMS-Struktur

Die **MCI \_ SET \_ PARMS-Struktur** enthält Informationen für den [**MCI \_ SET-Befehl.**](mci-set.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Zeitformat für das Gerät.

</dd> <dt>

**dwAudio**
</dt> <dd>

Audioausgabekanal.

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

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

