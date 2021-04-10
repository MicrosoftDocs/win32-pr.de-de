---
title: TBN_DROPDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Dropdown-Schaltfläche klickt Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- Windows-Steuerelemente für TBN_DROPDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949693"
---
# <a name="tbn_dropdown-notification-code"></a>TBN- \_ Dropdown-Benachrichtigungs Code

Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Dropdown-Schaltfläche klickt Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält. Bei diesem Benachrichtigungs Code sind nur die **HDR** -und **iItem** -Member dieser Struktur gültig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück:



| Rückgabecode                                                                                          | Beschreibung                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**tbddret ( \_ Standard)**</dt> </dl>      | Der Dropdown wurde behandelt.<br/>                                             |
| <dl> <dt>**tbddret \_ NODEFAULT**</dt> </dl>    | Die Dropdown-Dropdown-Anwendung wurde nicht behandelt.<br/>                                         |
| <dl> <dt>**tbddret- \_ behandelte**</dt> </dl> | Das Dropdown Feld wurde behandelt, aber die Schaltfläche wird wie eine reguläre Schaltfläche behandelt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dropdown Schaltflächen können Plain ([**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) -Stil) sein, einen Pfeil neben dem Schaltflächen Bild anzeigen ([**btns- \_ volledropdown**](toolbar-control-and-button-styles.md) -Stil) oder einen Pfeil anzeigen, der vom Bild getrennt ist ([**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) -Stil). Wenn ein getrennter Pfeil verwendet wird, wird die TBN- \_ Dropdown Liste nur gesendet, wenn der Benutzer auf den Pfeil Bereich der Schaltfläche klickt. Wenn der Benutzer auf den Hauptteil der Schaltfläche klickt, wird eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung mit der ID des Schaltflächen wie bei einer Standard Schaltfläche gesendet. Für die beiden anderen Stile der Dropdown Schaltfläche wird die TBN- \_ Dropdown Liste gesendet, wenn der Benutzer auf einen beliebigen Teil der Schaltfläche klickt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

