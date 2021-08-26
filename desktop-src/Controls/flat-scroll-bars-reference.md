---
title: Flache Bildlaufleiste
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die zum Steuern von flachen Scrollleisten verwendet werden.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf1c1d49bf4b54d65adbe784d1e4da62adfe35c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466597"
---
# <a name="flat-scroll-bar"></a>Flache Bildlaufleiste

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die zum Steuern von flachen Scrollleisten verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                    | Inhalte                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Flache Bildlaufleisten](flat-scroll-bars.md) | Microsoft Internet Explorer 4.0 hat eine neue visuelle Technologie namens flache Scrollleisten eingeführt. Funktionell verhalten sich flache Scrollleisten wie Standard-Scrollleisten. Der Unterschied besteht in der Anpassung der Darstellung im Größeren als bei Standard-Bildlaufleisten.<br/> |



 

### <a name="functions"></a>Functions




| Thema | Inhalte | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a> | Aktiviert oder deaktiviert eine oder beide Schaltflächen für die Richtung einer flachen Bildlaufleiste. Wenn für das Fenster keine flachen Bildlaufleisten initialisiert werden, ruft diese Funktion die <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>standardmäßige EnableScrollBar-Funktion</strong></a> auf. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a> | Ruft die Informationen für eine flache Scrollleiste ab. Wenn keine flachen Bildlaufleisten für das Fenster initialisiert werden, ruft diese Funktion die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo-Standardfunktion</strong></a> auf. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a> | Ruft die Strichposition in einer flachen Bildlaufleiste ab. Wenn für das Fenster keine flachen Bildlaufleisten initialisiert werden, ruft diese Funktion die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos-Standardfunktion</strong></a> auf. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a> | Ruft die Eigenschaften für eine flache Scrollleiste ab. Diese Funktion kann auch verwendet werden, um zu bestimmen, <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>ob InitializeFlatSB</strong></a> für dieses Fenster aufgerufen wurde. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a> | Ruft die Eigenschaften für eine flache Scrollleiste ab. Diese Funktion kann auch verwendet werden, um zu bestimmen, <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>ob InitializeFlatSB</strong></a> für dieses Fenster aufgerufen wurde.<blockquote>[!Note]<br />Dies ist identisch mit <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a> | Ruft den Bildlaufbereich für eine flache Scrollleiste ab. Wenn für das Fenster keine flachen Bildlaufleisten initialisiert werden, ruft diese Funktion die <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange-Standardfunktion</strong></a> auf. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a> | Legt die Informationen für eine flache Scrollleiste fest. Wenn für das Fenster keine flachen Bildlaufleisten initialisiert werden, ruft diese Funktion die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>Standardfunktion SetScrollInfo</strong></a> auf. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a> | Legt die aktuelle Position des Daumens in einer flachen Bildlaufleiste fest. Wenn für das Fenster keine flachen Bildlaufleisten initialisiert werden, ruft diese Funktion die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>Standardfunktion SetScrollPos</strong></a> auf. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a> | Legt die Eigenschaften für eine flache Scrollleiste fest. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a> | Legt den Bildlaufbereich einer flachen Scrollleiste fest. Wenn für das Fenster keine flachen Bildlaufleisten initialisiert werden, ruft diese Funktion die <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>Standardfunktion SetScrollRange</strong></a> auf. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a> | Blendet eine flache Scrollleiste ein oder aus. Wenn für das Fenster keine flachen Bildlaufleisten initialisiert werden, ruft diese Funktion die <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>standardmäßige ShowScrollBar-Funktion</strong></a> auf. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> | Initialisiert flache Bildlaufleisten für ein bestimmtes Fenster. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a> | Initialisiert flache Bildlaufleisten für ein bestimmtes Fenster. Das angegebene Fenster wird auf Standard-Scrollleisten zurückverwendet. <br /> | 




 

 

 





