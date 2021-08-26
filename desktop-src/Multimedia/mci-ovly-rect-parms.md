---
title: MCI_OVLY_RECT_PARMS-Struktur (Mciapi.h)
description: Die MCI \_ OVLY \_ RECT \_ PARMS-Struktur enthält Positionierungsinformationen für die Befehle MCI \_ PUT und MCI \_ WHERE für Videoüberlagerungsgeräte.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- MCI_OVLY_RECT_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfd55b2950f6d4268a9af5ee5bdc7fc9c378c4dbaeaa569406339263a2cf85e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039110"
---
# <a name="mci_ovly_rect_parms-structure"></a>MCI \_ OVLY \_ RECT \_ PARMS-Struktur

Die **MCI \_ OVLY \_ RECT \_ PARMS-Struktur** enthält Positionierungsinformationen für die [**Befehle MCI \_ PUT**](mci-put.md) und [**MCI \_ WHERE**](mci-where.md) für Videoüberlagerungsgeräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**Rc**
</dt> <dd>

Rechteck mit Positionierungsinformationen. [RECT-Strukturen](/previous-versions//ms536136(v=vs.85)) werden in MCI anders behandelt als in anderen Teilen von Windows. in MCI enthält **rc.right** die Breite des Rechtecks und **rc.bottom** die Höhe.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

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

[**MCI \_ PUT**](mci-put.md)
</dt> <dt>

[**MCI \_ WHERE**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[Rect](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

