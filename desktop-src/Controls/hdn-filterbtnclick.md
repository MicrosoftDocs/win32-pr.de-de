---
title: HDN_FILTERBTNCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster des Header Steuer Elements, wenn auf die Filter Schaltfläche geklickt wird, oder als Reaktion auf eine HDM- \_ Nachricht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- Windows-Steuerelemente für HDN_FILTERBTNCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858683"
---
# <a name="hdn_filterbtnclick-notification-code"></a>Hdn \_ filterbtnclick-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster des Header Steuer Elements, wenn auf die Filter Schaltfläche geklickt wird, oder als Reaktion auf eine [**HDM \_**](hdm-setitem.md) -Nachricht. Dieser Benachrichtigungs Code wird in Form einer [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmhdfilterbtnclick**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) -Struktur, die Informationen über das Header Steuerelement und die Header Filter Schaltfläche enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn Sie " **true**" zurückgeben, wird ein [Hdn- \_ FilterChange](hdn-filterchange.md) -Benachrichtigungs Code an das übergeordnete Fenster des Header Steuer Elements gesendet. Mit diesem Benachrichtigungs Code erhält das übergeordnete Fenster die Gelegenheit, seine Benutzeroberflächen Elemente zu synchronisieren. Gibt **false** zurück, wenn Sie nicht möchten, dass die Benachrichtigung gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Nmhdfilterbtnclick**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





