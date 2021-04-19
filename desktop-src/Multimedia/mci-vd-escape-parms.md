---
title: MCI_VD_ESCAPE_PARMS-Struktur (mciapi. h)
description: Die MCI-VD-escapeparameterstruktur \_ \_ \_ enthält den Befehl, der für den Befehl "MCI-Escapezeichen" an ein Gerät gesendet wird \_ .
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- MCI_VD_ESCAPE_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339959"
---
# <a name="mci_vd_escape_parms-structure"></a>MCI-VD-escapeparameterstruktur \_ \_ \_

Die **MCI- \_ VD \_ \_** -escapeparameterstruktur enthält den Befehl, der für den Befehl " [**MCI \_**](mci-escape.md) -Escapezeichen" an ein Gerät gesendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**lpstraucommand**
</dt> <dd>

Befehl, der an das Gerät gesendet werden soll.

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

[**MCI- \_ Escape**](mci-escape.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

