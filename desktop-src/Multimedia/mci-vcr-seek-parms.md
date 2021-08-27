---
title: MCI_VCR_SEEK_PARMS-Struktur (Vcr.h)
description: Die MCI \_ VCR \_ SEEK \_ PARMS-Struktur enthält Parameter für den MCI \_ SEEK-Befehl für Video-Cassette-Aufzeichnungen.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- MCI_VCR_SEEK_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee25352925681ef548310d9e009808499ce0a36f80472e50ee2a0daa71ed8dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038200"
---
# <a name="mci_vcr_seek_parms-structure"></a>MCI \_ VCR \_ SEEK \_ PARMS-Struktur

Die **MCI \_ VCR \_ SEEK \_ PARMS-Struktur** enthält Parameter für den [**MCI \_ SEEK-Befehl**](mci-seek.md) für Video-Cassette-Aufzeichnungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwTo**
</dt> <dd>

Position, nach der gesucht werden soll.

</dd> <dt>

**dwMark**
</dt> <dd>

Nummerierte Markierung, nach der gesucht werden soll.

</dd> <dt>

**dwAt**
</dt> <dd>

Zeit, zu der die Suche beginnt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Positionen werden im aktuellen Zeitformat angegeben.

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ SEEK**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

