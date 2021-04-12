---
title: MCI_OVLY_RECT_PARMS-Struktur (mciapi. h)
description: Die MCI \_ \_ -Struktur für den OVLY Rect \_ -Inhalt enthält Positionsinformationen für die MCI \_ Put-und MCI \_ -Befehle für Video Überlagerungs Geräte.
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
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475093"
---
# <a name="mci_ovly_rect_parms-structure"></a>MCI \_ OVLY \_ Rect- \_ Struktur

Die MCI-Struktur für den **\_ OVLY \_ \_ Rect** -Inhalt enthält Positionsinformationen für die [**MCI \_ Put**](mci-put.md) -und [**MCI \_**](mci-where.md) -Befehle für Video Überlagerungs Geräte.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**RC**
</dt> <dd>

Rechteck, das Positionsinformationen enthält. [Rect](/previous-versions//ms536136(v=vs.85)) -Strukturen werden in MCI anders behandelt als in anderen Teilen von Windows. in MCI enthält **RC. Right** die Breite des Rechtecks und **RC. Bottom** enthält die Höhe des Rechtecks.

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

[**MCI- \_ Put**](mci-put.md)
</dt> <dt>

[**MCI, \_ wobei**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[Rect](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

