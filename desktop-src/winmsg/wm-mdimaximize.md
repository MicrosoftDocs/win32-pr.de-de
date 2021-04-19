---
description: Eine Anwendung sendet die WM- \_ mdimaximiernachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu maximieren.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: WM_MDIMAXIMIZE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345705"
---
# <a name="wm_mdimaximize-message"></a>WM- \_ mdimaximiungsmeldung

Eine Anwendung sendet die **WM- \_ mdimaximiernachricht** an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu maximieren. Das System ändert die Größe des untergeordneten Fensters, damit der Client Bereich das Client Fenster ausfüllen muss. Das System platziert das Fenstermenü Symbol des untergeordneten Fensters an der rechten Position der Menüleiste des Frame Fensters und platziert das Wiederherstellungs Symbol des untergeordneten Fensters an der äußersten linken Position. Das System fügt den Text der Titelleiste des untergeordneten Fensters auch an die des Frame Fensters an.


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das untergeordnete MDI-Fenster, das maximiert werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **null**

Der Rückgabewert ist immer 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn ein MDI-Client Fenster eine Nachricht empfängt, die die Aktivierung der untergeordneten Fenster ändert, während das momentan aktive untergeordnete MDI-Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder her und maximiert das neu aktivierte untergeordnete Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WM- \_ mumgeleitet-Speicher**](wm-mdirestore.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




