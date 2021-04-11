---
title: MCI_SET_PARMS-Struktur (mciapi. h)
description: Die Struktur der MCI- \_ Set- \_ Parametern enthält Informationen für den MCI- \_ Befehl Set.
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
ms.openlocfilehash: 971affd319ecae817b9c1159ab0f307d0c2a5c91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040296"
---
# <a name="mci_set_parms-structure"></a>Struktur von MCI- \_ Set- \_ Parametern

Die Struktur der **MCI- \_ Set- \_ Parametern** enthält Informationen für den [**MCI-Befehl \_ Set**](mci-set.md) .

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

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwtimeformat**
</dt> <dd>

Das Zeitformat für das Gerät.

</dd> <dt>

**dwaudiodatei**
</dt> <dd>

Audioausgabechannel.

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

 

