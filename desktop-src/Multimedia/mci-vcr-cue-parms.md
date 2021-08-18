---
title: MCI_VCR_CUE_PARMS-Struktur (Vcr.h)
description: Die MCI \_ VCR \_ CUE \_ PARMS-Struktur enthält Parameter für den MCI \_ CUE-Befehl für Video-Cassette-Aufzeichnungen.
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- MCI_VCR_CUE_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff14bf6db2fee24b2cee426114b460dc5e4682bd00e14f7b68a91695bab1f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038240"
---
# <a name="mci_vcr_cue_parms-structure"></a>MCI \_ VCR \_ CUE \_ PARMS-Struktur

Die **MCI \_ VCR \_ CUE \_ PARMS-Struktur** enthält Parameter für den [**MCI \_ CUE-Befehl**](mci-cue.md) für Video-Cassette-Aufzeichnungen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhandle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position, aus der ein Hinweis entnommen werden soll.

</dd> <dt>

**dwTo**
</dt> <dd>

Position, zu der ein Hinweis zu machen ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI \_ CUE**](mci-cue.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

