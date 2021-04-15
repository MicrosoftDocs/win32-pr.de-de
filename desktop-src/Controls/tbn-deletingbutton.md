---
title: TBN_DELETINGBUTTON Meldung (kommstrg. h)
description: Wird von einem Symbolleisten-Steuerelement gesendet, wenn eine Schaltfläche gelöscht wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- Windows-Steuerelemente für TBN_DELETINGBUTTON Meldung
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26337fd1abc6c67351fe2b38e83ee7d90a11f6e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517510"
---
# <a name="tbn_deletingbutton-message"></a>TBN- \_ Delta Button-Meldung

Wird von einem Symbolleisten-Steuerelement gesendet, wenn eine Schaltfläche gelöscht wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur, die Informationen über die Schaltfläche enthält, die gelöscht wird. Bei diesem Benachrichtigungs Code sind nur die **HDR** -und **iItem** -Member dieser Struktur gültig. Der **iItem** -Member dieser Struktur enthält den Befehls Bezeichner der Schaltfläche, die gelöscht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





