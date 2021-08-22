---
title: HDN_DROPDOWN Benachrichtigungscode (Commctrl.h)
description: Wird von einem Headersteuerelement an sein übergeordnetes Element gesendet, wenn auf den Dropdownpfeil auf dem Headersteuerelement geklickt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5a7e423c40fa655a9eca0e5b97c20a2d61add1e6c0b7f66b65a69afdc32a55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435570"
---
# <a name="hdn_dropdown-notification-code"></a>\_HDN-DROPDOWN-Benachrichtigungscode

Wird von einem Headersteuerelement an sein übergeordnetes Element gesendet, wenn auf den Dropdownpfeil auf dem Headersteuerelement geklickt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) die Informationen zum Headersteuerelement enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das Beispiel im Abschnitt Syntax zeigt, wie der Benachrichtigungsempfänger **LPARAM** umgibt, um die [**NMHEADER-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) abzurufen. **WPARAM** enthält die ID des Steuerelements, das diese Nachricht sendet.

Diese Nachricht wird nur gesendet, wenn das HDF \_ SPLITBUTTON-Format für das Headerelement festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





