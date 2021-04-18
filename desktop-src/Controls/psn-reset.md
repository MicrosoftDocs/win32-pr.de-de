---
title: PSN_RESET Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass das Eigenschaften Blatt zerstört werden soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- Windows-Steuerelemente für PSN_RESET Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340314"
---
# <a name="psn_reset-notification-code"></a>\_Benachrichtigungs Code für PSN-zurück

Benachrichtigt eine Seite, dass das Eigenschaften Blatt zerstört werden soll. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Alle Änderungen, die seit dem letzten Benachrichtigungs Code für den [PSN \_](psn-apply.md) -Anwendungscode vorgenommen wurden, werden abgebrochen, außer im Fall von [**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), der diesen Benachrichtigungs Code nicht unterstützt.

Der **LPARAM** -Member der [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, auf die von *LPARAM* verwiesen wird, wird auf " **true** " festgelegt, wenn der Benutzer auf die Schaltfläche " **X** " in der oberen rechten Ecke des Eigenschaften Blatts geklickt hat. Der Wert ist **false** , wenn der Benutzer auf die Schaltfläche **Abbrechen** geklickt hat. Die **pshnotify** -Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.

Eine Anwendung kann diesen Benachrichtigungs Code als Gelegenheit zum Ausführen von Bereinigungs Vorgängen verwenden.

> [!Note]  
> Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code für die PSN-zurück Setzung gesendet wird. Versuchen Sie nicht, während der Verarbeitung dieses Benachrichtigungs Codes Seiten hinzuzufügen, zu entfernen oder einzufügen. Dies führt zu unvorhersehbaren Ergebnissen.

 

Beim Verarbeiten dieses Benachrichtigungs Codes dürfen Sie die [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) -Funktion nicht aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

