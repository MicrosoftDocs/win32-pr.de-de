---
title: MCI_GENERIC_PARMS-Struktur (mciapi. h)
description: Die generische MCI- \_ \_ Struktur enthält das Handle des Fensters, das Benachrichtigungs Meldungen empfängt. Diese Struktur wird für MCI-befehlsnachrichten verwendet, die leere Parameterlisten aufweisen.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- MCI_GENERIC_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476230"
---
# <a name="mci_generic_parms-structure"></a>Generische MCI- \_ \_ paramemstruktur

Die **\_ generische \_ MCI** -Struktur enthält das Handle des Fensters, das Benachrichtigungs Meldungen empfängt. Diese Struktur wird für MCI-befehlsnachrichten verwendet, die leere Parameterlisten aufweisen.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **MCI \_ \_** --, Close-und **MCI- \_ Merkmals \_** Struktur-Strukturen sind identisch mit der **generischen MCI-Struktur von \_ \_ para** Metern.

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

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

