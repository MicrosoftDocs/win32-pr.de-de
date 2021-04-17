---
title: MCI_VCR_SEEK_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Such \_ Parameter enthält Parameter für den MCI- \_ Suchbefehl für Video-Kassetten-Recorder.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- MCI_VCR_SEEK_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476005"
---
# <a name="mci_vcr_seek_parms-structure"></a>Struktur der MCI- \_ VCR- \_ Such \_ Teilwerte

Die Struktur der **MCI- \_ VCR- \_ Such \_** Parameter enthält Parameter für den [**MCI- \_ Such**](mci-seek.md) Befehl für Video-Kassetten-Recorder.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
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

</dd> <dt>

**dwmark**
</dt> <dd>

Nummerierte Markierung, nach der gesucht werden soll.

</dd> <dt>

**dwat**
</dt> <dd>

Zeitpunkt, zu dem die Suche beginnt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Positionen werden im aktuellen Zeitformat angegeben.

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



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

 

