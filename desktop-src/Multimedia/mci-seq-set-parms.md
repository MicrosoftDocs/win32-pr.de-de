---
title: MCI_SEQ_SET_PARMS -Struktur (Mciapi.h)
description: Die MCI \_ SEQ \_ SET \_ PARMS-Struktur enthält Informationen für den MCI \_ SET-Befehl für SEQUENCEr-Geräte.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS-Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffb96cfd2f652bf989673bad68c95c6765034d2105fa554efee057faf099a9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374968"
---
# <a name="mci_seq_set_parms-structure"></a>MCI \_ SEQ \_ SET \_ PARMS-Struktur

Die **MCI \_ SEQ \_ SET \_ PARMS-Struktur** enthält Informationen für den [**MCI \_ SET-Befehl**](mci-set.md) für SEQUENCEr-Geräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Das Zeitformat des Sequencers.

</dd> <dt>

**dwAudio**
</dt> <dd>

Audioausgabekanal.

</dd> <dt>

**dwTempo**
</dt> <dd>

Tempo.

</dd> <dt>

**dwPort**
</dt> <dd>

Port.

</dd> <dt>

**dwSklave**
</dt> <dd>

Synchronisierungstyp, der vom Sequencer für untergeordneten Vorgang verwendet wird.

</dd> <dt>

**dwMaster**
</dt> <dd>

Der Synchronisierungstyp, der vom Sequencer für den Mastervorgang verwendet wird.

</dd> <dt>

**dwOffset**
</dt> <dd>

Datenoffset.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ SET**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

