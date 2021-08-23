---
title: MCI_VCR_STEP_PARMS-Struktur (Vcr.h)
description: Die MCI \_ VCR \_ STEP \_ PARMS-Struktur enthält Parameter für den MCI \_ STEP-Befehl für Video-Cassette-Aufzeichnungen.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- MCI_VCR_STEP_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f25e79903a694b6537e88d1c58994d1f39ccf958ea95f40f571a267239a055e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783829"
---
# <a name="mci_vcr_step_parms-structure"></a>MCI \_ VCR \_ STEP \_ PARMS-Struktur

Die **MCI \_ VCR \_ STEP \_ PARMS-Struktur** enthält Parameter für den [**MCI \_ STEP-Befehl**](mci-step.md) für Video-Cassette-Aufzeichnungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwFrames**
</dt> <dd>

Anzahl der Zu springende Frames (die Länge eines einzelnen Schritts), während der [**MCI \_ STEP-Befehl**](mci-step.md) den Inhalt vorwärts oder rückwärts durchschritten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern in dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* von [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

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

[**\_MCI-SCHRITT**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

