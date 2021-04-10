---
title: Benachrichtigungs Code für NM_NCHITTEST (Rebar) (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine WM- \_ nchittest-Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Windows-Steuerelemente für die NM_NCHITTEST (Info Leiste)
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105098"
---
# <a name="nm_nchittest-rebar-notification-code"></a>NM \_ nchittest (Info Leiste)-Benachrichtigungs Code

Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) -Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die Informationen über den Benachrichtigungs Code enthält. Der **dwitemspec** -Member enthält den BandIndex, über den die Treffer Testnachricht aufgetreten ist, und das **PT** -Element enthält die Maus Koordinaten der Treffer Testnachricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, damit die Überprüfung die Standard Verarbeitung der Treffer Testnachricht durchführen kann, oder gibt einen der HT-Werte zurück, der \* unter [**WM \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) dokumentiert ist, um die standardmäßige Treffer Testverarbeitung zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

