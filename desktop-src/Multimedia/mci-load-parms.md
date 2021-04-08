---
title: MCI_LOAD_PARMS-Struktur (MMSYSTEM. h)
description: Die Struktur des MCI- \_ Lade- \_ Parametern enthält den Dateinamen, der für den Befehl MCI Load geladen werden soll \_ .
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- MCI_LOAD_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742945"
---
# <a name="mci_load_parms-structure"></a>Struktur von MCI- \_ Lade- \_ Parametern

Die Struktur des **MCI- \_ Lade- \_ Parametern** enthält den Dateinamen, der für den Befehl [**MCI \_**](mci-load.md) Load geladen werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**lpFileName**
</dt> <dd>

Der Name der zu ladenden Datei.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI- \_ Auslastung**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

