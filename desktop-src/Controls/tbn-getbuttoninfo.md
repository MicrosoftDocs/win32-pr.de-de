---
title: TBN_GETBUTTONINFO Benachrichtigungs Code (kommctrl. h)
description: Ruft Informationen zur Symbolleisten Anpassung ab und benachrichtigt das übergeordnete Fenster der Symbolleiste über alle Änderungen, die an der Symbolleiste vorgenommen werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- Windows-Steuerelemente für TBN_GETBUTTONINFO Benachrichtigungs
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
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956873"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>TBN- \_ getbuttoninfo-Benachrichtigungs Code

Ruft Informationen zur Symbolleisten Anpassung ab und benachrichtigt das übergeordnete Fenster der Symbolleiste über alle Änderungen, die an der Symbolleiste vorgenommen werden. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur. Das **iItem-Element** gibt einen NULL basierten Index an, der die Anzahl der Schaltflächen bereitstellt. das Dialogfeld Symbolleiste anpassen wird sowohl als verfügbar als auch auf der Symbolleiste angezeigt. Der **pszText** -Member gibt die Adresse des aktuellen Schaltflächen Texts an, und **cchtext** gibt seine Länge in Zeichen an. Die Anwendung sollte die Struktur mit Informationen über die Schaltfläche Auffüllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn Schaltflächen Informationen in die angegebene-Struktur kopiert wurden, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Das Symbolleisten-Steuerelement ordnet einen Puffer zu, und der Empfänger (übergeordnetes Fenster) muss den Text in diesen Puffer kopieren. Der **cchtext** -Member enthält die Länge des Puffers, der von der Symbolleiste zugewiesen wird, wenn TBN \_ getbuttoninfo an das übergeordnete Fenster gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TBN \_ Getbuttoninfow** (Unicode) und **TBN \_ getbuttoninfoa** (ANSI)<br/>       |



 

 





