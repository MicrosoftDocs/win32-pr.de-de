---
title: MCI_STATUS_PARMS-Struktur (Mciapi.h)
description: Die MCI \_ STATUS \_ PARMS-Struktur enthält Informationen für den MCI \_ STATUS-Befehl.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2685ec70f10dc8dcecb0149f3bcf1af6c9814dd360e8f7e185d31710c24d5527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138096"
---
# <a name="mci_status_parms-structure"></a>MCI \_ STATUS \_ PARMS-Struktur

Die **MCI \_ STATUS \_ PARMS-Struktur** enthält Informationen für den [**MCI \_ STATUS-Befehl.**](mci-status.md)

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwReturn**
</dt> <dd>

Enthält Informationen zur Rückgabe.

</dd> <dt>

**dwItem**
</dt> <dd>

Funktion, die abgefragt wird.

</dd> <dt>

**dwTrack**
</dt> <dd>

Länge oder Anzahl von Spuren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das MCI \_ STATUS \_ ITEM-Flag muss im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) festgelegt werden, um den **dwItem-Member** zu überprüfen, der eine der Konstanten enthalten sollte, die angeben, welche Statusinformationen angefordert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**\_MCI-STATUS**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

