---
title: MCI_VCR_STEP_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Schritt- \_ Parameter enthält Parameter für den MCI- \_ Schritt Befehl für Video-Kassetten-Recorder.
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
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040219"
---
# <a name="mci_vcr_step_parms-structure"></a>Struktur von MCI- \_ VCR- \_ Schritt- \_ Parametern

Die Struktur der **MCI- \_ VCR- \_ Schritt \_** -Parameter enthält Parameter für den [**MCI- \_ Schritt**](mci-step.md) Befehl für Video-Kassetten-Recorder.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwframes**
</dt> <dd>

Die Anzahl der zu über springenden Frames (die Länge eines einzelnen Schritts), wenn der [**MCI- \_ Schritt**](mci-step.md) Befehl den Inhalt vorwärts oder rückwärts durchläuft.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Elementen in dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter von [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) fest, um die Elemente zu validieren.

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

[**MCI- \_ Schritt**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

