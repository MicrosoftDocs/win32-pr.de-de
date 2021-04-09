---
title: MCI_VCR_SETAUDIO_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR \_ - \_ setaudioparameter enthält Parameter für den MCI \_ setaudiobefehl für Video-Kassetten-Recorder.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- MCI_VCR_SETAUDIO_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858708"
---
# <a name="mci_vcr_setaudio_parms-structure"></a>MCI \_ VCR \_ -setaudioparamemstruktur \_

Die Struktur der **MCI- \_ VCR \_ -setaudioparameter \_** enthält Parameter für den [**MCI \_ setaudiobefehl**](mci-setaudio.md) für Video-Kassetten-Recorder.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwtrack**
</dt> <dd>

Audiospur.

</dd> <dt>

**dwto**
</dt> <dd>

Typ der Eingabe-oder überwachten Eingabe.

</dd> <dt>

**dwnumber**
</dt> <dd>

Audioeingabe (des Typs, der im **dwto** -Member angegeben ist), der verwendet werden soll.

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

[**MCI \_ -setaudiodatei**](mci-setaudio.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

