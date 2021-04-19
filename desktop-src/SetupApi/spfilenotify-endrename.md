---
description: Die spfilenotify \_ endrename-Benachrichtigung wird an die Rückruf Routine gesendet, wenn die Warteschlange einen Umbenennungs Vorgang abschließt. Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: SPFILENOTIFY_ENDRENAME Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a316d4dfe72ee9eb7d85fdb70eb90e1cf3d3f463
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352340"
---
# <a name="spfilenotify_endrename-message"></a>Spfilenotify \_ endrename-Meldung

Die **spfilenotify \_ endrename** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn die Warteschlange einen Umbenennungs Vorgang abschließt. Diese Benachrichtigung wird gesendet, auch wenn der Benutzer abbricht oder wenn ein Fehler auftritt.


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param1* 
</dt> <dd>

Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur. Der **Win32Error** -Member der **FilePath** -Struktur gibt das Ergebnis des Kopiervorgangs an.

</dd> <dt>

*Param2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht](overview.md)
</dt> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**Setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




