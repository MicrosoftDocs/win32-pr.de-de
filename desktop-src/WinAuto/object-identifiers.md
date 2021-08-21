---
title: Objektbezeichner (Winuser.h)
description: In diesem Thema werden die Microsoft Active Accessibility Objektbezeichner und 32-Bit-Werte beschrieben, die Kategorien von barrierefreien Objekten innerhalb eines Fensters identifizieren.
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
ms.openlocfilehash: 7b91bf70333d4ba7d607e465851f7f217aec43b0a081ec020017321fe30a7ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565065"
---
# <a name="object-identifiers-winuserh"></a>Objektbezeichner (Winuser.h)

In diesem Thema werden die Microsoft Active Accessibility Objektbezeichner und 32-Bit-Werte beschrieben, die *Kategorien* von barrierefreien Objekten innerhalb eines Fensters identifizieren. Microsoft Active Accessibility Server und Microsoft Benutzeroberflächenautomatisierung-Anbieter verwenden die Objektbezeichner, um das Objekt zu bestimmen, auf das eine [**WM \_ GETOBJECT-Nachrichtenanforderung**](wm-getobject.md) verweist.

Clients erhalten diese Werte in ihrer [*WinEventProc-Rückruffunktion*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) und verwenden sie, um Teile eines Fensters zu identifizieren. Server verwenden diese Werte, um die entsprechenden Teile eines Fensters zu identifizieren, wenn [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) aufgerufen oder auf die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) reagiert wird.

Server können benutzerdefinierte Objekt-IDs definieren, um andere Objektkategorien in ihren Anwendungen zu identifizieren. Benutzerdefinierten Objekt-IDs müssen positive Werte zugewiesen werden, da Microsoft Active Accessibility null und alle negativen Werte für die folgenden Standardobjektbezeichner reserviert.

Die folgenden Konstanten werden in winuser.h definiert:



| Konstante                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**\_OBJID-WARNUNG**</dt> </dl>                                     | Eine Warnung, die einem Fenster oder einer Anwendung zugeordnet ist. Vom System bereitgestellte Meldungsfelder sind die einzigen Benutzeroberflächenelemente, die Ereignisse mit diesem Objektbezeichner senden. Serveranwendungen können die **AccessibleObjectFrom**_X-Funktionen_ nicht mit diesem Objektbezeichner verwenden. Dies ist ein bekanntes Problem mit Microsoft Active Accessibility.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**OBJID \_ CARET**</dt> </dl>                                     | Die Texteinfügeleiste (Caretzeichen) im Fenster.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**\_OBJID-CLIENT**</dt> </dl>                                  | Der Clientbereich des Fensters. In den meisten Fällen steuert das Betriebssystem die Frameelemente, und das Clientobjekt enthält alle Elemente, die von der Anwendung gesteuert werden. Server verarbeiten nur die [**WM \_ GETOBJECT-Nachrichten,**](wm-getobject.md) in denen *das lParam* OBJID \_ CLIENT, OBJID \_ WINDOW oder ein benutzerdefinierter Objektbezeichner ist.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**OBJID \_ CURSOR**</dt> </dl>                                  | Der Mauszeiger. Das System enthält nur einen Mauszeiger und ist kein untergeordnetes Element eines Fensters.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**OBJID \_ HSCROLL**</dt> </dl>                               | Die horizontale Bildlaufleiste des Fensters.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**OBJID \_ NATIVEOM**</dt> </dl>                            | Als Reaktion auf diesen Objektbezeichner können Anwendungen von Drittanbietern ihr eigenes Objektmodell verfügbar machen. Anwendungen von Drittanbietern können eine beliebige COM-Schnittstelle als Reaktion auf diesen Objektbezeichner zurückgeben.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**\_OBJID-MENÜ**</dt> </dl>                                        | Die Menüleiste des Fensters.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**OBJID \_ QUERYCLASSNAMEIDX**</dt> </dl> | Ein Objektbezeichner, der Oleacc.dll intern verwendet. Weitere Informationen finden Sie unter [Anhang F: Objektbezeichnerwerte für OBJID \_ QUERYCLASSNAMEIDX.](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md)<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**OBJID \_ SIZELP**</dt> </dl>                            | Der Größen-Klammer des Fensters: eine optionale Rahmenkomponente in der unteren rechten Ecke des Fensterrahmens.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**\_OBJID-SOUND**</dt> </dl>                                     | Ein Soundobjekt. Soundobjekte verfügen nicht über Bildschirmpositionen oder untergeordnete Elemente, aber sie verfügen über Namens- und Zustandsattribute. Sie sind untergeordnete Elemente der Anwendung, die den Sound abspielt.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**OBJID \_ SYSMENU**</dt> </dl>                               | Das Systemmenü des Fensters.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**OBJID \_ TITLEBAR**</dt> </dl>                            | Die Titelleiste des Fensters.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**OBJID \_ VSCROLL**</dt> </dl>                               | Die vertikale Bildlaufleiste des Fensters.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**\_OBJID-FENSTER**</dt> </dl>                                  | Das Fenster selbst anstelle eines untergeordneten Objekts.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

 





