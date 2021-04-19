---
title: Header Steuerelement Stile (kommctrl. h)
description: Header Steuerelemente haben einige Stile, die in diesem Abschnitt beschrieben werden, um die Darstellung und das Verhalten des Steuer Elements zu bestimmen. Sie legen die anfänglichen Stile fest, wenn Sie das Header Steuerelement erstellen.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369661"
---
# <a name="header-control-styles"></a>Header Steuerelement Stile

Header Steuerelemente haben einige Stile, die in diesem Abschnitt beschrieben werden, um die Darstellung und das Verhalten des Steuer Elements zu bestimmen. Sie legen die anfänglichen Stile fest, wenn Sie das Header Steuerelement erstellen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <dt><strong>HDS_BUTTONS</strong></dt> </dl></td>
<td style="text-align: left;">Jedes Element im-Steuerelement sieht und verhält sich wie eine Schaltfläche "Push". Dieser Stil ist nützlich, wenn eine Anwendung eine Aufgabe ausführt, wenn der Benutzer auf ein Element im Header Steuerelement klickt. Beispielsweise könnte eine Anwendung Informationen in den Spalten unterschiedlich sortieren, je nachdem, auf welches Element der Benutzer klickt. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <dt><strong>HDS_DRAGDROP</strong></dt> </dl></td>
<td style="text-align: left;">Ermöglicht die Neuanordnung von Header Elementen per Drag & Drop. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <dt><strong>HDS_FILTERBAR</strong></dt> </dl></td>
<td style="text-align: left;">Fügen Sie eine Filter Leiste als Teil des Standard Header-Steuer Elements ein. In dieser Leiste können Benutzer bequem einen Filter auf die Anzeige anwenden. Aufrufe an <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> ergeben eine neue Größe für das Steuerelement und bewirken, dass die Listenansicht aktualisiert wird. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <dt><strong>HDS_FLAT</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,0 und</a>höher. Bewirkt, dass das Header Steuerelement flach gezeichnet wird, wenn das Betriebssystem im klassischen Modus ausgeführt wird. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll Version 6 ist nicht Verteil Bar, aber Sie ist in Windows enthalten. Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <dt><strong>HDS_FULLDRAG</strong></dt> </dl></td>
<td style="text-align: left;">Bewirkt, dass das Header Steuerelement auch dann Spalten Inhalte anzeigt, wenn der Benutzer die Größe einer Spalte ändert. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <dt><strong>HDS_HIDDEN</strong></dt> </dl></td>
<td style="text-align: left;">Gibt ein Header Steuerelement an, das ausgeblendet werden soll. In diesem Stil wird das Steuerelement nicht ausgeblendet. Wenn Sie die <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> Nachricht stattdessen an ein Header Steuerelement mit dem HDS_HIDDEN Format senden, gibt das Steuerelement im <strong>CY</strong> -Element der <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>Windows</strong></a> -Struktur 0 (null) zurück. Anschließend blenden Sie das Steuerelement aus, indem Sie die Höhe auf NULL festlegen. Dies kann hilfreich sein, wenn Sie das-Steuerelement als Informationscontainer anstelle eines visuellen Steuer Elements verwenden möchten. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <dt><strong>HDS_HORZ</strong></dt> </dl></td>
<td style="text-align: left;">Erstellt ein Header Steuerelement mit horizontaler Ausrichtung. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <dt><strong>HDS_HOTTRACK</strong></dt> </dl></td>
<td style="text-align: left;">Aktiviert die Hot-Nachverfolgung. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <dt><strong>HDS_CHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,00 und</a>höher. Ermöglicht das Platzieren von Kontrollkästchen für Header Elemente. Weitere Informationen finden Sie unter dem <strong>fmt</strong> -Member von <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <dt><strong>HDS_NOSIZING</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,00 und</a>höher. Der Benutzer kann den unter Teiler nicht auf das Header Steuerelement ziehen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <dt><strong>HDS_OVERFLOW</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,00 und</a>höher. Eine Schaltfläche wird angezeigt, wenn nicht alle Elemente innerhalb des Rechtecks des Header Steuer Elements angezeigt werden können. Wenn Sie auf diese Schaltfläche klicken, wird eine <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> Benachrichtigung gesendet.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Wenn Sie die Stile nach dem Erstellen des Steuer Elements abrufen und ändern möchten, verwenden Sie die Funktionen [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) und [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



