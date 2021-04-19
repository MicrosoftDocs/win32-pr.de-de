---
title: Objekt Bezeichner (Winuser. h)
description: In diesem Thema werden die Microsoft Active Accessibility-Objekt Bezeichner, 32-Bit-Werte beschrieben, die Kategorien von zugänglichen Objekten innerhalb eines Fensters identifizieren.
ms.assetid: dc1603f8-29e5-4acd-817a-c6957feaff6c
topic_type:
- apiref
api_name:
- OBJID_ALERT
- OBJID_CARET
- OBJID_CLIENT
- OBJID_CURSOR
- OBJID_HSCROLL
- OBJID_NATIVEOM
- OBJID_MENU
- OBJID_QUERYCLASSNAMEIDX
- OBJID_SIZEGRIP
- OBJID_SOUND
- OBJID_SYSMENU
- OBJID_TITLEBAR
- OBJID_VSCROLL
- OBJID_WINDOW
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa2cf2099c5177be6f295ef6455646762525b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356449"
---
# <a name="object-identifiers-winuserh"></a>Objekt Bezeichner (Winuser. h)

In diesem Thema werden die Microsoft Active Accessibility-Objekt Bezeichner, 32-Bit-Werte beschrieben, die *Kategorien* von zugänglichen Objekten innerhalb eines Fensters identifizieren. Microsoft Active Accessibility-Server und Microsoft-Benutzeroberflächenautomatisierungs-Anbieter verwenden die Objekt Bezeichner, um das Objekt zu ermitteln, auf das eine [**WM- \_ GetObject**](wm-getobject.md) -Nachrichten Anforderung verweist.

Clients erhalten diese Werte in Ihrer [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) -Rückruffunktion und verwenden Sie, um Teile eines Fensters zu identifizieren. Server verwenden diese Werte, um die entsprechenden Teile eines Fensters zu identifizieren, wenn [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) aufgerufen wird, oder wenn auf die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht reagiert wird.

Server können benutzerdefinierte Objekt-IDs definieren, um andere Kategorien von Objekten innerhalb Ihrer Anwendungen zu identifizieren. Benutzerdefinierten Objekt-IDs müssen positive Werte zugewiesen werden, da Microsoft Active Accessibility NULL und alle negativen Werte für die folgenden Standard Objekt-IDs reserviert.

Die folgenden Konstanten sind in winuser. h definiert:



| Konstante                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**objID- \_ Warnung**</dt> </dl>                                     | Eine Warnung, die einem Fenster oder einer Anwendung zugeordnet ist. Die vom System bereitgestellten Meldungs Felder sind die einzigen Benutzeroberflächen Elemente, die Ereignisse mit diesem Objekt Bezeichner senden. Server Anwendungen können die **accessibleobjectfrom**_X_ -Funktionen mit diesem Objekt Bezeichner nicht verwenden. Dies ist ein bekanntes Problem mit Microsoft Active Accessibility.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**objID- \_ Caretzeichen**</dt> </dl>                                     | Die Text Einfügeleiste (Einfügemarke) im-Fenster.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**objID- \_ Client**</dt> </dl>                                  | Der Client Bereich des Fensters. In den meisten Fällen steuert das Betriebssystem die Frame-Elemente, und das Client Objekt enthält alle Elemente, die von der Anwendung gesteuert werden. Server verarbeiten nur die [**WM- \_ GetObject**](wm-getobject.md) -Nachrichten, bei denen *LPARAM* den objID- \_ Client, das objID- \_ Fenster oder einen benutzerdefinierten Objekt Bezeichner hat.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**objID- \_ Cursor**</dt> </dl>                                  | Der Mauszeiger. Es ist nur ein Mauszeiger im System vorhanden, und es ist kein untergeordnetes Element eines Fensters.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**objID \_ HScroll**</dt> </dl>                               | Die horizontale Schiebe Leiste des Fensters.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**objID \_ nativeom**</dt> </dl>                            | Als Reaktion auf diesen Objekt Bezeichner können Anwendungen von Drittanbietern Ihr eigenes Objektmodell verfügbar machen. Anwendungen von Drittanbietern können eine beliebige com-Schnittstelle als Reaktion auf diesen Objekt Bezeichner zurückgeben.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**objID- \_ Menü**</dt> </dl>                                        | Die Menüleiste des Fensters.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**objID \_ queryclassnameidx**</dt> </dl> | Ein Objekt Bezeichner, der von Oleacc.dll intern verwendet wird. Weitere Informationen finden Sie unter [Anhang F: objektbezeichnerwerte für objID \_ queryclassnameidx](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**objID \_ SizeGrip**</dt> </dl>                            | Der Größen Zieh Punkt des Fensters: eine optionale Frame Komponente, die sich in der unteren rechten Ecke des Fensterrahmens befindet.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**objID- \_ Sound**</dt> </dl>                                     | Ein Sound Objekt. Sound Objekte weisen keine Bildschirm Positionen oder untergeordneten Elemente auf, Sie verfügen jedoch über Attribute für Name und Status. Dabei handelt es sich um untergeordnete Elemente der Anwendung, die den Sound wieder gibt.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**objID ( \_ sysmenu)**</dt> </dl>                               | Das Systemmenü des Fensters.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**objID- \_ TitleBar**</dt> </dl>                            | Die Titelleiste des Fensters.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**objID- \_ VScroll**</dt> </dl>                               | Die vertikale Schiebe Leiste des Fensters.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**objID-Fenster \_**</dt> </dl>                                  | Das Fenster selbst anstelle eines untergeordneten Objekts.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

 





