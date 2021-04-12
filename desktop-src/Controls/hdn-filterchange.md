---
title: HDN_FILTERCHANGE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster des Header Steuer Elements, dass die Attribute eines Header Steuerelement Filters geändert oder bearbeitet werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- Windows-Steuerelemente für HDN_FILTERCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475378"
---
# <a name="hdn_filterchange-notification-code"></a>Hdn- \_ FilterChange-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster des Header Steuer Elements, dass die Attribute eines Header Steuerelement Filters geändert oder bearbeitet werden. Dieser Benachrichtigungs Code wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Header Element enthält, einschließlich der Attribute, die gerade geändert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HDM \_ setfilterchangetimeout**](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





