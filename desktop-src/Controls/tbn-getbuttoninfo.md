---
title: TBN_GETBUTTONINFO Benachrichtigungscode (Commctrl.h)
description: Ruft Anpassungsinformationen zur Symbolleiste ab und benachrichtigt das übergeordnete Fenster der Symbolleiste über alle Änderungen, die an der Symbolleiste vorgenommen werden. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32a73b7da3efee0b1bb1ba829cf40356e6060a5f7e7fdfcc2467e2cca32226a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876860"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>TBN \_ GETBUTTONINFO-Benachrichtigungscode

Ruft Anpassungsinformationen zur Symbolleiste ab und benachrichtigt das übergeordnete Fenster der Symbolleiste über alle Änderungen, die an der Symbolleiste vorgenommen werden. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTOOLBAR-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Das **iItem-Element** gibt einen nullbasierten Index an, der die Anzahl der Schaltflächen bereitstellt, die im Dialogfeld Symbolleiste anpassen sowohl als verfügbar als auch auf der Symbolleiste angezeigt werden. Der **pszText-Member** gibt die Adresse des aktuellen Schaltflächentexts an, und **cchText** gibt seine Länge in Zeichen an. Die Anwendung sollte die Struktur mit Informationen über die Schaltfläche füllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn Schaltflächeninformationen in die angegebene Struktur kopiert wurden, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Das Symbolleisten-Steuerelement ordnet einen Puffer zu, und der Empfänger (übergeordnetes Fenster) muss den Text in diesen Puffer kopieren. Das **cchText-Element** enthält die Länge des Puffers, der von der Symbolleiste zugeordnet wird, wenn TBN \_ GETBUTTONINFO an das übergeordnete Fenster gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TBN \_ GETBUTTONINFOW** (Unicode) und **TBN \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 





