---
title: MCI_VCR_SETVIDEO_PARMS -Struktur (Vcr.h)
description: Die MCI VCR SETVIDEO PARMS-Struktur enthält Parameter für den \_ \_ \_ \_ MCI-Befehl SETVIDEO für Video cassette-Aufzeichnungen.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- MCI_VCR_SETVIDEO_PARMS-Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf260804a6e993ba133ca450a51802a0f43db3aa3d0e557ba684b8a86bcfb7dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784130"
---
# <a name="mci_vcr_setvideo_parms-structure"></a>MCI \_ VCR \_ SETVIDEO \_ PARMS-Struktur

Die **MCI \_ VCR \_ SETVIDEO \_ PARMS-Struktur** enthält Parameter für den [**\_ MCI-Befehl SETVIDEO**](mci-setvideo.md) für Video cassette-Aufzeichnungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwTrack**
</dt> <dd>

Betroffene Spur.

</dd> <dt>

**dwTo**
</dt> <dd>

Typ der Eingabe oder überwachten Eingabe.

</dd> <dt>

**dwNumber**
</dt> <dd>

Zu verwendende Videoeingabe (des im **dwTo-Member** angegebenen Typs).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ SETVIDEO**](mci-setvideo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

