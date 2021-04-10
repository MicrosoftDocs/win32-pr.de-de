---
title: PSN_SETACTIVE Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass Sie im Begriff ist, aktiviert zu werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- Windows-Steuerelemente für PSN_SETACTIVE Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956716"
---
# <a name="psn_setactive-notification-code"></a>PSN- \_ SETACTIVE-Benachrichtigungs Code

Benachrichtigt eine Seite, dass Sie im Begriff ist, aktiviert zu werden. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält. Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt. Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, um die Aktivierung zu akzeptieren, oder-1 zum Aktivieren der nächsten oder der vorherigen Seite (abhängig davon, ob der Benutzer auf die Schaltfläche " **weiter** " oder " **zurück** " geklickt hat). Um die Aktivierung auf eine bestimmte Seite festzulegen, geben Sie den Ressourcen Bezeichner der Seite zurück.

## <a name="remarks"></a>Bemerkungen

Der \_ Benachrichtigungs Code "PSN SETACTIVE" wird gesendet, bevor die Seite sichtbar ist. Eine Anwendung kann diesen Benachrichtigungs Code verwenden, um Daten auf der Seite zu initialisieren.

> [!Note]  
> Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code "PSN SETACTIVE" gesendet wird. Versuchen Sie nicht, während der Verarbeitung dieses Benachrichtigungs Codes Seiten hinzuzufügen, zu entfernen oder einzufügen. Dies führt zu unvorhersehbaren Ergebnissen.

 

Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem DWL \_ msgresult-Wert verwenden, und die Dialogfeld Prozedur muss **true** zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

