---
title: MCI_RECORD_PARMS -Struktur (Mciapi.h)
description: Die MCI \_ RECORD \_ PARMS-Struktur enthält Positionierungsinformationen für den MCI \_ RECORD-Befehl.
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- MCI_RECORD_PARMS-Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c531b5b186a6119a22cafc4e252424ace2e388b2545461b440cd7957694494b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039080"
---
# <a name="mci_record_parms-structure"></a>MCI \_ RECORD \_ PARMS-Struktur

Die **MCI \_ RECORD \_ PARMS-Struktur** enthält Positionierungsinformationen für den [**MCI \_ RECORD-Befehl.**](mci-record.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position, von der aus sie abspielt werden soll.

</dd> <dt>

**dwTo**
</dt> <dd>

Position, an der abspielt werden soll.

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

[**MCI \_ RECORD**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

