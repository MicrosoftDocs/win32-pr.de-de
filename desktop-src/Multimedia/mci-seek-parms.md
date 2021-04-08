---
title: MCI_SEEK_PARMS-Struktur (mciapi. h)
description: Die MCI \_ - \_ suchparametenstruktur enthält Positionsinformationen für den MCI \_ Seek-Befehl.
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- MCI_SEEK_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c31f419b2458dedc19c6533e8f0f7fade97026e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740488"
---
# <a name="mci_seek_parms-structure"></a>Struktur der MCI- \_ Such \_ Teilwerte

Die **MCI \_ - \_ suchparametenstruktur** enthält Positionsinformationen für den [**MCI \_ Seek**](mci-seek.md) -Befehl.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwto**
</dt> <dd>

Position, an der gesucht werden soll.

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

[**MCI- \_ Suche**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

