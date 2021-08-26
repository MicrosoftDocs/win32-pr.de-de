---
title: MCI_VCR_RECORD_PARMS-Struktur (Vcr.h)
description: Die MCI \_ VCR \_ RECORD \_ PARMS-Struktur enthält Parameter für den MCI \_ RECORD-Befehl für Video-Cassette-Aufzeichnungen.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b613c2b64bae1395b3fc402816145c0ef690801b9fd6402201198f7ff28a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038230"
---
# <a name="mci_vcr_record_parms-structure"></a>MCI \_ VCR \_ RECORD \_ PARMS-Struktur

Die **MCI \_ VCR \_ RECORD \_ PARMS-Struktur** enthält Parameter für den [**MCI \_ RECORD-Befehl**](mci-record.md) für Video-Cassette-Aufzeichnungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position, aus der wiedergegeben werden soll.

</dd> <dt>

**dwTo**
</dt> <dd>

Position, an der wiedergegeben werden soll.

</dd> <dt>

**dwAt**
</dt> <dd>

Zeitwert, der sich auf den [**MCI \_ RECORD-**](mci-record.md) oder [**MCI \_ CUE-Befehl**](mci-cue.md) auswirkt. Für **MCI \_ RECORD** ist dies der Zeitpunkt, zu dem die Aufzeichnung beginnt. Für **MCI \_ CUE** ist dies der Zeitpunkt, zu dem das gerät mit dem Cuing die in **dwFrom** angegebene Position erreicht.

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

[**MCI \_ CUE**](mci-cue.md)
</dt> <dt>

[**MCI \_ RECORD**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

