---
title: MCI_INFO_PARMS -Struktur (Mciapi.h)
description: Die MCI \_ INFO \_ PARMS-Struktur enthält Informationen für den MCI \_ INFO-Befehl.
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- MCI_INFO_PARMS-Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2415fe0234c1a5b553a8b55d785febd82ebdd770f8c297bfc483549a1aa2a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375015"
---
# <a name="mci_info_parms-structure"></a>MCI \_ INFO \_ PARMS-Struktur

Die **MCI \_ INFO \_ PARMS-Struktur** enthält Informationen für den [**MCI \_ INFO-Befehl.**](mci-info.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Puffer für die Rückgabezeichenfolge.

</dd> <dt>

**dwRetSize**
</dt> <dd>

Größe der Rückgabezeichenfolge in Zeichen.

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

[**\_MCI-INFORMATIONEN**](mci-info.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

