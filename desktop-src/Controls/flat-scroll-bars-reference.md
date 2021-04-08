---
title: Flatscrollleiste
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die zum Steuern von flatscrollleisten verwendet werden.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855715"
---
# <a name="flat-scroll-bar"></a>Flatscrollleiste

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die zum Steuern von flatscrollleisten verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                    | Inhalte                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Flache Scrollleisten](flat-scroll-bars.md) | Microsoft Internet Explorer 4,0 führte eine neue visuelle Technologie mit dem Namen "flatscrollleisten" ein. Funktionale, flache Schiebe leisten Verhalten sich genau wie Standard Scrollleisten. Der Unterschied besteht darin, dass Sie Ihre Darstellung in größerem Umfang als Standard Scrollleisten anpassen können.<br/> |



 

### <a name="functions"></a>Functions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Inhalte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></td>
<td>Aktiviert oder deaktiviert eine oder beide Richtungs Schaltflächen der flatscrollleiste. Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>enablescrollbar</strong></a> auf. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></td>
<td>Ruft die Informationen für eine flatscrollleiste ab. Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die standardmäßige <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>getscrollinfo</strong></a> -Funktion auf. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></td>
<td>Ruft die Ziehpunkt Position in einer flachen Bild Lauf Leiste ab. Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die standardmäßige <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>getscrollpos</strong></a> -Funktion auf. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></td>
<td>Ruft die Eigenschaften für eine flatscrollleiste ab. Diese Funktion kann auch verwendet werden, um zu bestimmen, ob <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>initializeflatsb</strong></a> für dieses Fenster aufgerufen wurde. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></td>
<td>Ruft die Eigenschaften für eine flatscrollleiste ab. Diese Funktion kann auch verwendet werden, um zu bestimmen, ob <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>initializeflatsb</strong></a> für dieses Fenster aufgerufen wurde.
<blockquote>
[!Note]<br />
Dies ist mit <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>identisch.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></td>
<td>Ruft den Bild Laufbereich für eine flatscrollleiste ab. Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die standardmäßige <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>getscrollrange</strong></a> -Funktion auf. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></td>
<td>Legt die Informationen für eine flache Bild Lauf Leiste fest. Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion " <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>setScrollInfo</strong></a> " auf. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></td>
<td>Legt die aktuelle Position des Zieh Punkts auf einer flachen Bild Lauf Leiste fest. Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>setscrollpos</strong></a> auf. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></td>
<td>Legt die Eigenschaften für eine flache Bild Lauf Leiste fest. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></td>
<td>Legt den scrollbereich einer flachen Bild Lauf Leiste fest. Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>setscrollrange</strong></a> auf. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></td>
<td>Zeigt eine flache Schiebe Leiste an oder blendet sie aus. Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion " <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollbar</strong></a> " auf. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>Initializeflatsb</strong></a></td>
<td>Initialisiert flatscrollleisten für ein bestimmtes Fenster. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>Uninitializeflatsb</strong></a></td>
<td>Hebt die Initialisierung der flatscrollleisten für ein bestimmtes Fenster auf. Das angegebene Fenster wird auf Standard Scrollleisten zurückgesetzt. <br/></td>
</tr>
</tbody>
</table>



 

 

 





