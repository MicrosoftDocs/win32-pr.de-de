---
description: Wird verwendet, um private Nachrichten zu definieren, in der Regel im Format WM \_ APP+x, wobei x ein ganzzahliger Wert ist.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01c2f09bef9ef479cfa5bd0bb56760fd17196087992276b2caa1daf7616fea9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931820"
---
# <a name="wm_app"></a>\_WM-APP

Wird verwendet, um private Nachrichten zu definieren, in der Regel im **Format WM \_ APP** + *x*, wobei *x* ein ganzzahliger Wert ist.

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a>Hinweise

Die **WM \_ APP-Konstante** wird verwendet, um zwischen Nachrichtenwerten, die für die Verwendung durch das System reserviert sind, und Werten zu unterscheiden, die von einer Anwendung verwendet werden können, um Nachrichten innerhalb einer privaten Fensterklasse zu senden. Im Folgenden finden Sie die verfügbaren Nachrichtennummernbereiche.



| Range                                                 | Bedeutung                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0 bis [**WM \_ USER**](wm-user.md) –1<br/>   | Nachrichten, die für die Verwendung durch das System reserviert sind.<br/>            |
| [**WM \_ BENUTZER**](wm-user.md) über 0x7FFF<br/> | Ganzzahlige Nachrichten zur Verwendung durch private Fensterklassen.<br/> |
| **WM \_ APP** über 0xBFFF<br/>                 | Nachrichten, die von Anwendungen verwendet werden können.<br/>         |
| 0xC000 durch 0xFFFF<br/>                      | Zeichenfolgenmeldungen zur Verwendung durch Anwendungen.<br/>            |
| Größer als 0xFFFF<br/>                        | Vom System reserviert.<br/>                             |



 

Nachrichtennummern im ersten Bereich (0 bis [**WM \_ USER**](wm-user.md) –1) werden vom System definiert. Werte in diesem Bereich, die nicht explizit definiert sind, werden vom System reserviert.

Nachrichtennummern im zweiten Bereich ([**WM \_ USER**](wm-user.md) bis 0x7FFF) können von einer Anwendung definiert und verwendet werden, um Nachrichten innerhalb einer privaten Fensterklasse zu senden. Diese Werte können nicht verwendet werden, um Meldungen zu definieren, die in einer Anwendung sinnvoll sind, da einige vordefinierte Fensterklassen bereits Werte in diesem Bereich definieren. Beispielsweise können vordefinierte Steuerelementklassen wie **BUTTON,** **EDIT,** **LISTBOX** und **COMBOBOX** diese Werte verwenden. Nachrichten in diesem Bereich sollten nicht an andere Anwendungen gesendet werden, es sei denn, die Anwendungen wurden für den Austausch von Nachrichten und das Anfügen der gleichen Bedeutung an die Nachrichtennummern entwickelt.

Nachrichtennummern im dritten Bereich (0x8000 bis 0xBFFF) sind für Anwendungen verfügbar, die als private Nachrichten verwendet werden können. Nachrichten in diesem Bereich stehen nicht in Konflikt mit Systemmeldungen.

Nachrichtennummern im vierten Bereich (0xC000 bis 0xFFFF) werden zur Laufzeit definiert, wenn eine Anwendung die [**RegisterWindowMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) aufruft, um eine Nachrichtennummer für eine Zeichenfolge abzurufen. Alle Anwendungen, die dieselbe Zeichenfolge registrieren, können die zugeordnete Nachrichtennummer zum Austauschen von Nachrichten verwenden. Die tatsächliche Nachrichtennummer ist jedoch keine Konstante und kann zwischen verschiedenen Sitzungen nicht als identisch angenommen werden.

Nachrichtennummern im fünften Bereich (größer als 0xFFFF) werden vom System reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**\_WM-BENUTZER**](wm-user.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Nachrichten und Nachrichtenwarteschlangen](messages-and-message-queues.md)
</dt> </dl>

 

 
