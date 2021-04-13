---
title: TVN_SINGLEEXPAND Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement mit dem singleexpand-Stil des TVs gesendet, \_ Wenn der Benutzer ein Strukturelement mit einem einzigen Mausklick öffnet oder schließt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- Windows-Steuerelemente für TVN_SINGLEEXPAND Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475744"
---
# <a name="tvn_singleexpand-notification-code"></a>TVN \_ singleexpand-Benachrichtigungs Code

Wird von einem Strukturansicht-Steuerelement mit [**dem \_ singleexpand**](tree-view-control-window-styles.md) -Stil des TVs gesendet, wenn der Benutzer ein Strukturelement mit einem einzigen Mausklick öffnet oder schließt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Rückgabe von tvnret \_ Default, damit das Standardverhalten auftritt. Um das Standardverhalten zu ändern, geben Sie Folgendes ein:



| Rückgabecode                                                                                    | Beschreibung                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**tvnret \_ skipold**</dt> </dl> | Überspringen Sie die Standard Verarbeitung des Elements, dessen Auswahl aufgehoben wird.<br/> |
| <dl> <dt>**tvnret \_ skipnew**</dt> </dl> | Überspringen Sie die Standard Verarbeitung des ausgewählten Elements.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Um die Standard Verarbeitung ausgewählter und nicht ausgewählter Elemente zu überspringen, geben Sie sowohl tvnret \_ skipold als auch tvnret \_ skipnew zurück, indem Sie Sie mit einem logischen OR kombinieren.

Dieser Benachrichtigungs Code wird nur von Strukturansicht-Steuerelementen gesendet, die den [**\_ singleexpand**](tree-view-control-window-styles.md) -Stil "TVs" aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





