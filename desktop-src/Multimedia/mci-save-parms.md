---
title: MCI_SAVE_PARMS-Struktur (mciapi. h)
description: Die MCI \_ - \_ Struktur zum Speichern von Parametern enthält die Dateinamen Informationen für den MCI- \_ Befehl "Save".
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- MCI_SAVE_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341781"
---
# <a name="mci_save_parms-structure"></a>MCI- \_ Struktur zum Speichern von \_ Parametern

Die **MCI-Struktur zum \_ Speichern von \_ Parametern** enthält die Dateinamen Informationen für den MCI-Befehl " [**\_ Save**](mci-save.md) ".

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**lpFileName**
</dt> <dd>

Der Name der zu speichernden Datei.

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

[**MCI- \_ Speicherung**](mci-save.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

