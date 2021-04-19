---
title: MCI_VCR_RECORD_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Daten Satz \_ Parameter enthält Parameter für den MCI- \_ Datensatz-Befehl für Video-Kassetten-Recorder.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339142"
---
# <a name="mci_vcr_record_parms-structure"></a>Struktur von MCI \_ VCR- \_ Daten Satz- \_ Parametern

Die Struktur der **MCI- \_ VCR- \_ Daten Satz \_** Parameter enthält Parameter für den [**MCI- \_ Datensatz**](mci-record.md) -Befehl für Video-Kassetten-Recorder.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwfrom**
</dt> <dd>

Wiedergabe Position

</dd> <dt>

**dwto**
</dt> <dd>

Position der Wiedergabe.

</dd> <dt>

**dwat**
</dt> <dd>

Zeitwert, der sich auf den [**MCI- \_ Datensatz**](mci-record.md) oder den [**MCI \_**](mci-cue.md) -Hinweis Befehl auswirkt. Bei einem **MCI- \_ Datensatz** ist dies der Zeitpunkt, zu dem die Aufzeichnung beginnt. Bei **MCI \_**-Hinweis ist dies die Zeit, zu der das cubegerät die in **dwfrom** angegebene Position erreicht.

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

[**MCI \_ -Hinweis**](mci-cue.md)
</dt> <dt>

[**MCI- \_ Datensatz**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

