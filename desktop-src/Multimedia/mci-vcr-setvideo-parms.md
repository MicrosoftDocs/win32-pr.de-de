---
title: MCI_VCR_SETVIDEO_PARMS Struktur (VCR. h)
description: Die Struktur der MCI \_ VCR- \_ setvideo \_ -Parameter enthält Parameter für den MCI \_ setvideo-Befehl für Video-Kassetten-Recorder.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- MCI_VCR_SETVIDEO_PARMS Struktur Windows Multimedia
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
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859188"
---
# <a name="mci_vcr_setvideo_parms-structure"></a>Struktur von MCI \_ VCR- \_ setvideo- \_ Parametern

Die Struktur der **MCI \_ VCR- \_ setvideo \_** -Parameter enthält Parameter für den [**MCI \_ setvideo**](mci-setvideo.md) -Befehl für Video-Kassetten-Recorder.

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

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwtrack**
</dt> <dd>

Betroffener Titel.

</dd> <dt>

**dwto**
</dt> <dd>

Typ der Eingabe-oder überwachten Eingabe.

</dd> <dt>

**dwnumber**
</dt> <dd>

Die für zu verwendende Video Eingabe (des Typs, der im **dwto** -Member angegeben ist).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

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

[**MCI- \_ setvideo**](mci-setvideo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

