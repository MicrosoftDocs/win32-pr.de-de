---
title: MCI_SEQ_SET_PARMS-Struktur (mciapi. h)
description: Die Struktur des MCI \_ Seq- \_ Set-Parametern \_ enthält Informationen zum MCI- \_ Befehl Set für die Komponenten von MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS Struktur Windows Multimedia
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
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949534"
---
# <a name="mci_seq_set_parms-structure"></a>Struktur von MCI \_ Seq- \_ Set- \_ Parametern

Die Struktur des **MCI \_ Seq- \_ Set- \_ Parametern** enthält Informationen zum [**MCI-Befehl \_ Set**](mci-set.md) für die Komponenten von MIDI Sequencer.

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

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwtimeformat**
</dt> <dd>

Das Zeitformat von Sequencer.

</dd> <dt>

**dwaudiodatei**
</dt> <dd>

Audioausgabechannel.

</dd> <dt>

**dwtempo**
</dt> <dd>

Lern.

</dd> <dt>

**dwport**
</dt> <dd>

Port.

</dd> <dt>

**dwslave**
</dt> <dd>

Der Synchronisierungstyp, der vom Sequencer für den untergeordneten Vorgang verwendet wird.

</dd> <dt>

**dwmaster**
</dt> <dd>

Der Synchronisierungstyp, der vom Sequencer für den Master Vorgang verwendet wird.

</dd> <dt>

**dwOffset**
</dt> <dd>

Daten Offset.

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

[**MCI- \_ Gruppe**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

