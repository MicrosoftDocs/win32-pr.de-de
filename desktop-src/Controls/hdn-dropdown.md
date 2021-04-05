---
title: HDN_DROPDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header Steuerelement an das übergeordnete Element gesendet, wenn auf den Dropdown Pfeil im Header Steuerelement geklickt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- Windows-Steuerelemente für HDN_DROPDOWN Benachrichtigungs
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
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859352"
---
# <a name="hdn_dropdown-notification-code"></a>Benachrichtigungs Code für Hdn- \_ Dropdown

Wird von einem Header Steuerelement an das übergeordnete Element gesendet, wenn auf den Dropdown Pfeil im Header Steuerelement geklickt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das Beispiel im Abschnitt Syntax zeigt, wie der Benachrichtigungs Empfänger **LPARAM** zum Abrufen der [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur umwirft. **WParam** enthält die ID des Steuer Elements, das diese Nachricht sendet.

Diese Meldung wird nur gesendet, wenn \_ für das Header Element Style HDF SplitButton festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





