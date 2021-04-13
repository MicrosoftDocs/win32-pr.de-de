---
description: Wird verwendet, um private Nachrichten zu definieren, in der Regel in der Form WM \_ app + x, wobei x ein ganzzahliger Wert ist.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216963"
---
# <a name="wm_app"></a>WM- \_ App

Wird verwendet, um private Nachrichten zu definieren, in der Regel in der Form **WM \_ App** + *x*, wobei *x* ein ganzzahliger Wert ist.

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a>Bemerkungen

Die **\_ App** -Konstante der WM wird verwendet, um zwischen Nachrichten Werten zu unterscheiden, die für die Verwendung durch das System reserviert sind, und Werte, die von einer Anwendung verwendet werden können, um Nachrichten innerhalb einer privaten Fenster Klasse zu senden. Im folgenden finden Sie die verfügbaren Bereiche der Nachrichtennummern.



| Range                                                 | Bedeutung                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0 bis [**WM \_ Benutzer**](wm-user.md) – 1<br/>   | Nachrichten, die für die Verwendung durch das System reserviert sind<br/>            |
| [**WM \_ Benutzer**](wm-user.md) über 0x7FFF<br/> | Ganzzahlige Nachrichten, die von privaten Fenster Klassen verwendet werden.<br/> |
| **WM \_ App** über 0xbfff<br/>                 | Nachrichten, die für die Verwendung durch Anwendungen verfügbar sind.<br/>         |
| 0xc000 bis 0xFFFF<br/>                      | Zeichen folgen Nachrichten zur Verwendung durch Anwendungen.<br/>            |
| Größer als 0xFFFF<br/>                        | Vom System reserviert.<br/>                             |



 

Die Nachrichtennummern im ersten Bereich (0 bis [**WM \_**](wm-user.md) – 1) werden vom System definiert. Werte in diesem Bereich, die nicht explizit definiert sind, werden vom System reserviert.

Nachrichtennummern im zweiten Bereich ([**WM- \_ Benutzer**](wm-user.md) bis 0x7FFF) können definiert und von einer Anwendung verwendet werden, um Nachrichten innerhalb einer privaten Fenster Klasse zu senden. Diese Werte können nicht verwendet werden, um Nachrichten zu definieren, die in einer Anwendung sinnvoll sind, da einige vordefinierte Fenster Klassen bereits Werte in diesem Bereich definieren. Beispielsweise können von vordefinierten Steuerelement Klassen wie **Button**, **Edit**, **ListBox** und **ComboBox** diese Werte verwendet werden. Nachrichten in diesem Bereich sollten nicht an andere Anwendungen gesendet werden, es sei denn, die Anwendungen wurden zum Austauschen von Nachrichten und zum Anfügen derselben Bedeutung an die Nachrichtennummern entwickelt.

Die Nachrichtennummern im dritten Bereich (0X8000 bis 0xbfff) sind für Anwendungen verfügbar, die als private Nachrichten verwendet werden. Nachrichten in diesem Bereich stehen nicht in Konflikt mit Systemmeldungen.

Die Nachrichtennummern im vierten Bereich (0xc000 bis 0xFFFF) werden zur Laufzeit definiert, wenn eine Anwendung die [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) -Funktion aufruft, um eine Nachrichtennummer für eine Zeichenfolge abzurufen. Alle Anwendungen, die dieselbe Zeichenfolge registrieren, können die zugeordnete Nachrichtennummer zum Austauschen von Nachrichten verwenden. Die tatsächliche Nachrichtennummer ist jedoch keine Konstante und kann nicht davon ausgegangen werden, dass Sie zwischen verschiedenen Sitzungen identisch ist.

Die Nachrichtennummern im fünften Bereich (größer als 0xFFFF) werden vom System reserviert.

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

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**WM- \_ Benutzer**](wm-user.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Nachrichten und Nachrichten Warteschlangen](messages-and-message-queues.md)
</dt> </dl>

 

 
