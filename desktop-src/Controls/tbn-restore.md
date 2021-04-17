---
title: TBN_RESTORE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste wieder hergestellt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- Windows-Steuerelemente für TBN_RESTORE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478084"
---
# <a name="tbn_restore-notification-code"></a>TBN- \_ Wiederherstellungs Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste wieder hergestellt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtbrestore**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung sollte NULL als Antwort auf den ersten **TBN- \_ Wiederherstellungs** Benachrichtigungs Code zurückgeben, der zu Beginn des Wiederherstellungs Vorgangs empfangen wurde, damit die Schaltflächen Informationen weiterhin wieder hergestellt werden. Wenn die Anwendung einen Wert ungleich 0 (null) zurückgibt, wird der Wiederherstellungs Vorgang abgebrochen.

## <a name="remarks"></a>Bemerkungen

Die Anwendung empfängt diesen Benachrichtigungs Code einmal zu Beginn des Wiederherstellungs Vorgangs und einmal für jede Schaltfläche. Mit diesem Benachrichtigungs Code können Sie die Informationen aus dem Datenstrom extrahieren, den Sie zuvor gespeichert haben. Wenn Sie keine Informationen gespeichert haben, ignorieren Sie den Benachrichtigungs Code. Eine ausführlichere Erläuterung zur Handhabung der **TBN- \_ Wiederherstellung** finden Sie unter [Symbolleisten Anpassung](toolbar-controls-overview.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





