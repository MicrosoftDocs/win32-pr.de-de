---
title: MCI_LOAD_PARMS -Struktur (Mmsystem.h)
description: Die MCI \_ LOAD \_ PARMS-Struktur enthält den Dateinamen, der für den MCI LOAD-Befehl \_ geladen werden soll.
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- MCI_LOAD_PARMS-Struktur Windows Multimedia
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
ms.openlocfilehash: d52a5c875bbbfff6f94857bc7337a0cba1473571bfdb8edc8ccfa8f3f1a471fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375005"
---
# <a name="mci_load_parms-structure"></a>MCI \_ LOAD \_ PARMS-Struktur

Die **MCI \_ LOAD \_ PARMS-Struktur** enthält den Dateinamen, der für den [**MCI LOAD-Befehl \_ geladen werden**](mci-load.md) soll.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**lpfilename**
</dt> <dd>

Name der zu ladenden Datei.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmsystem.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ LOAD**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

