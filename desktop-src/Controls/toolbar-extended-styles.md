---
title: Erweiterte Toolbar-Stile (kommctrl. h)
description: In diesem Abschnitt werden die von Symbolleisten-Steuerelementen unterstützten erweiterten Stile aufgelistet
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354111"
---
# <a name="toolbar-extended-styles"></a>Erweiterte Toolbar-Stile

In diesem Abschnitt werden die von Symbolleisten-Steuerelementen unterstützten erweiterten Stile aufgelistet



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
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 4,71</a>. Dieser Stil ermöglicht, dass Schaltflächen über einen separaten Dropdown Pfeil verfügen. Schaltflächen, die den <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> Stil aufweisen, werden in einem separaten Abschnitt rechts von der Schaltfläche mit einem Dropdown Pfeil gezeichnet. Wenn auf den Pfeil geklickt wird, wird nur der Pfeil Teil der Schaltfläche dedrückt, und das Symbolleisten-Steuerelement sendet einen <a href="tbn-dropdown.md">TBN_DROPDOWN</a> Benachrichtigungs Code, um die Anwendung aufzufordern, das Dropdown Menü anzuzeigen. Wenn auf den Hauptteil der Schaltfläche geklickt wird, sendet das Symbolleisten-Steuerelement eine WM_COMMAND Meldung mit der ID der Schaltfläche. Die Anwendung antwortet normalerweise, indem der erste Befehl im Menü gestartet wird.<br/> Es gibt viele Situationen, in denen Sie möglicherweise nur einige der Dropdown Schaltflächen auf einer Symbolleiste mit getrennten Pfeilen verwenden möchten. Legen Sie zu diesem Zweck den TBSTYLE_EX_DRAWDDARROWS erweiterten Stil fest. Weisen Sie diese Schaltflächen, die keine getrennten Pfeile aufweisen, <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> Stil zu. Für Schaltflächen mit diesem Stil wird neben dem Bild ein Pfeil angezeigt. Der Pfeil wird jedoch nicht getrennt. wenn auf einen beliebigen Teil der Schaltfläche geklickt wird, sendet das Symbolleisten-Steuerelement einen <a href="tbn-dropdown.md">TBN_DROPDOWN</a> Benachrichtigungs Code. Um das Neuzeichnen von Problemen zu vermeiden, sollte dieser Stil festgelegt werden, bevor das ToolBar-Steuerelement sichtbar wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 5,81</a>. Dieser Stil verbirgt teilweise abgeschnittene Schaltflächen. Dieser Stil wird am häufigsten für Symbolleisten verwendet, die Teil eines Grund leisten-Steuer Elements sind. Wenn ein benachbartes Band einen Teil einer Schaltfläche abdeckt, wird die Schaltfläche nicht angezeigt. Wenn das Feld für die Bereichs Weitergabe jedoch den <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> Stil hat, wird die Schaltfläche im Dropdown Menü von Chevron angezeigt. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6</a>. Dieser Stil erfordert, dass die Symbolleiste doppelt gepuffert wird. Die doppelte Pufferung ist ein Mechanismus, der erkennt, wenn sich die Symbolleiste geändert hat. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll Version 6 ist nicht Verteil Bar, aber in Windows oder höher enthalten. Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 5,81</a>. Mit diesem Stil können Sie Text für alle Schaltflächen festlegen, ihn aber nur für diese Schaltflächen mit dem <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> Schaltflächen Stil anzeigen. Der <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> Stil muss ebenfalls festgelegt werden. Wenn eine Schaltfläche keinen Text anzeigt, muss die Anwendung normalerweise <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> oder <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> verarbeiten, um eine QuickInfo anzuzeigen. Beim erweiterten TBSTYLE_EX_MIXEDBUTTONS Stil wird Text, der festgelegt, aber nicht auf einer Schaltfläche angezeigt wird, automatisch als QuickInfo-Text der Schaltfläche verwendet. Die Anwendung muss nur TBN_GETINFOTIP oder oder TTN_GETDISPINFO verarbeiten, wenn Sie mehr Flexibilität bei der Angabe des QuickInfo-Texts benötigt. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 5,82</a>. <strong>Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</strong> Dieser Stil gibt der Symbolleiste eine vertikale Ausrichtung und organisiert die Symbolleisten Schaltflächen in Spalten. Die Schaltflächen werden vertikal vertikal dargestellt, bis eine Schaltfläche die umgebende Höhe der Symbolleiste überschreitet (siehe <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), und anschließend wird eine neue Spalte erstellt. Die Symbolleiste fließt auf diese Weise, bis alle Schaltflächen positioniert sind. Um dieses Format zu verwenden, muss der TBSTYLE_EX_VERTICAL Stil ebenfalls festgelegt werden. <br/>
<blockquote>
[!Note]<br />
Dieser Stil wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht unterstützt. Außerdem ist dieser Stil nicht in "kommctrl. h" definiert. Fügen Sie die folgende Definition zu den Quelldateien Ihrer Anwendung hinzu, um diesen Stil zu verwenden: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 5,82</a>. <strong>Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.</strong> Dieser Stil gibt der Symbolleiste eine vertikale Ausrichtung. Die Symbolleisten Schaltflächen werden von oben nach unten statt horizontal weitergeleitet. <br/>
<blockquote>
[!Note]<br />
Dieser Stil wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht unterstützt. Außerdem ist dieser Stil nicht in "kommctrl. h" definiert. Fügen Sie die folgende Definition zu den Quelldateien Ihrer Anwendung hinzu, um diesen Stil zu verwenden: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Um einen erweiterten Stil festzulegen, senden Sie das Symbolleisten-Steuerelement an eine [**TB- \_ SetExtendedStyle**](tb-setextendedstyle.md) -Nachricht. Wenn Sie bestimmen möchten, welche erweiterten Stile aktuell festgelegt sind, senden Sie eine [**TB- \_ GetExtendedStyle**](tb-getextendedstyle.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





