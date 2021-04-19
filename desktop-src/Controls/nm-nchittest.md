---
title: NM_NCHITTEST Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine WM- \_ nchittest-Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- Windows-Steuerelemente für NM_NCHITTEST Benachrichtigungs
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
ms.openlocfilehash: f8af39fd792ecb9aeb463957f49f5722737e6ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338737"
---
# <a name="nm_nchittest-notification-code"></a>NM \_ nchittest-Benachrichtigungs Code

Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) -Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die Informationen über den Benachrichtigungs Code enthält. Der *PT* -Member enthält die Maus Koordinaten der Treffer Testnachricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Sofern nicht anders angegeben, wird NULL zurückgegeben, damit das Steuerelement die Standard Verarbeitung der Treffer Testnachricht ausführen kann, oder einen der HT-Werte zurückgeben, der \* unter [**WM \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) dokumentiert ist, um die standardmäßige Treffer Testverarbeitung zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

