---
description: Wird verwendet, um private Nachrichten für die Verwendung durch private Fensterklassen zu definieren, in der Regel im Format OCM \_ \_ BASE+x, wobei x ein ganzzahliger Wert ist.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (Olectl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa3713d8a7b7447430e914e2582089244a417b1c
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588057"
---
# <a name="ocm__base"></a>OCM \_ \_ BASE

Wird verwendet, um private Nachrichten für die Verwendung durch private Fensterklassen zu definieren, in der Regel im Format **OCM \_ \_ BASE** + *x*, wobei *x* ein ganzzahliger Wert ist.

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a>Bemerkungen

Im Folgenden werden die Bereiche von Nachrichtennummern angezeigt.



| Range                                                 | Bedeutung                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0 bis [**WM \_ USER**](wm-user.md)-1<br/>   | Nachrichten, die für die Verwendung durch das System reserviert sind.<br/>            |
| [**WM \_ USER**](wm-user.md) über 0x7FFF<br/> | Ganzzahlige Nachrichten für die Verwendung durch private Fensterklassen.<br/> |
| [**WM \_ APP**](wm-app.md) über 0xBFFF<br/>   | Nachrichten, die für die Verwendung durch Anwendungen verfügbar sind.<br/>         |
| 0xC000 über 0xFFFF<br/>                      | Zeichenfolgenmeldungen zur Verwendung durch Anwendungen.<br/>            |
| Größer als 0xFFFF<br/>                        | Vom System reserviert.<br/>                             |



 

Nachrichtennummern im ersten Bereich (0 bis [**WM \_ USER**](wm-user.md)  1) werden vom System definiert. Werte in diesem Bereich, die nicht explizit definiert sind, werden vom System reserviert.

Nachrichtennummern im zweiten Bereich [**(WM \_ USER**](wm-user.md) bis 0x7FFF) können von einer Anwendung definiert und verwendet werden, um Nachrichten innerhalb einer privaten Fensterklasse zu senden. Diese Werte können nicht verwendet werden, um Nachrichten zu definieren, die in einer Anwendung sinnvoll sind, da einige vordefinierte Fensterklassen bereits Werte in diesem Bereich definieren. Vordefinierte Steuerelementklassen wie **BUTTON,** **EDIT,** **LISTBOX** und **COMBOBOX** können diese Werte beispielsweise verwenden. Nachrichten in diesem Bereich sollten nicht an andere Anwendungen gesendet werden, es sei denn, die Anwendungen wurden zum Austauschen von Nachrichten und zum Anfügen der gleichen Bedeutung an die Nachrichtennummern entwickelt.

Nachrichtennummern im dritten Bereich (0x8000 bis 0xBFFF) sind für Anwendungen verfügbar, die als private Nachrichten verwendet werden können. Nachrichten in diesem Bereich verursachen keinen Konflikt mit Systemmeldungen.

Nachrichtennummern im vierten Bereich (0xC000 bis 0xFFFF) werden zur Laufzeit definiert, wenn eine Anwendung die [**RegisterWindowMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) aufruft, um eine Nachrichtennummer für eine Zeichenfolge abzurufen. Alle Anwendungen, die dieselbe Zeichenfolge registrieren, können die zugeordnete Nachrichtennummer zum Austauschen von Nachrichten verwenden. Die tatsächliche Nachrichtennummer ist jedoch keine Konstante und kann nicht davon ausgegangen werden, dass sie zwischen verschiedenen Sitzungen identisch ist.

Nachrichtennummern im fünften Bereich (größer als 0xFFFF) werden vom System reserviert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Olectl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**\_WM-APP**](wm-app.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Nachrichten und Nachrichtenwarteschlangen](messages-and-message-queues.md)
</dt> </dl>

 

