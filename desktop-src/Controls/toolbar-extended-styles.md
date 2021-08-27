---
title: Erweiterte Stile der Symbolleiste (CommCtrl.h)
description: In diesem Abschnitt werden die erweiterten Stile aufgelistet, die von Symbolleistensteuerelementen unterstützt werden.
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
ms.openlocfilehash: 71e242426269d4049b913a41910d325c360886f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476781"
---
# <a name="toolbar-extended-styles"></a>Erweiterte Stile der Symbolleiste

In diesem Abschnitt werden die erweiterten Stile aufgelistet, die von Symbolleistensteuerelementen unterstützt werden.




| Konstante | BESCHREIBUNG | 
|----------|-------------|
| <span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt></dl> | <a href="common-control-versions.md">Version 4.71.</a> Mit diesem Stil können Schaltflächen über einen separaten Dropdownpfeil verfügen. Schaltflächen mit dem <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> Stil werden mit einem Dropdownpfeil in einem separaten Abschnitt rechts neben der Schaltfläche gezeichnet. Wenn auf den Pfeil geklickt wird, wird nur der Pfeilteil der Schaltfläche eingeblendet, und das Symbolleistensteuerelement sendet einen <a href="tbn-dropdown.md">TBN_DROPDOWN</a> Benachrichtigungscode, um die Anwendung aufzufordern, das Dropdownmenü anzuzeigen. Wenn auf den Hauptteil der Schaltfläche geklickt wird, sendet das Symbolleisten-Steuerelement eine WM_COMMAND Meldung mit der ID der Schaltfläche. Die Anwendung antwortet normalerweise, indem sie den ersten Befehl im Menü startet.<br /> Es gibt viele Situationen, in denen Sie möglicherweise nur einige der Dropdownschaltflächen auf einer Symbolleiste mit getrennten Pfeilen verwenden möchten. Legen Sie dazu die TBSTYLE_EX_DRAWDDARROWS erweiterten Stil fest. Weisen Sie den Schaltflächen, die keine getrennten Pfeile aufweisen, den <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> Stil zu. Bei Schaltflächen mit diesem Stil wird neben dem Bild ein Pfeil angezeigt. Der Pfeil ist jedoch nicht getrennt, und wenn auf einen Teil der Schaltfläche geklickt wird, sendet das Symbolleistensteuerelement einen <a href="tbn-dropdown.md">TBN_DROPDOWN</a> Benachrichtigungscode. Um Neumalierungsprobleme zu vermeiden, sollte dieser Stil festgelegt werden, bevor das Symbolleistensteuerelement sichtbar wird.<br /> | 
| <span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Version 5.81.</a> Dieser Stil blendet teilweise abgeschnittene Schaltflächen aus. Die gängigste Verwendung dieses Stils ist für Symbolleisten, die Teil eines Rebar-Steuerelements sind. Wenn ein angrenzendes Band einen Teil einer Schaltfläche verdeckt, wird die Schaltfläche nicht angezeigt. Wenn das Leistenband jedoch den <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>stil RBBS_USECHEVRON</strong></a> hat, wird die Schaltfläche im Dropdownmenü des Chevrons angezeigt. <br /> | 
| <span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Version 6</a>. Für diesen Stil muss die Symbolleiste doppelt gepuffert werden. Die doppelte Pufferung ist ein Mechanismus, der erkennt, wenn sich die Symbolleiste geändert hat. <br /><blockquote>[!Note]<br />Comctl32.dll Version 6 ist nicht verteilbar, aber in Windows oder höher enthalten. Um Comctl32.dll Version 6 zu verwenden, geben Sie sie in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen.</a></blockquote><br /> | 
| <span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Version 5.81.</a> Mit diesem Stil können Sie Text für alle Schaltflächen festlegen, aber nur für diese Schaltflächen mit dem <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> Schaltflächenstil anzeigen. Der <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> Stil muss ebenfalls festgelegt werden. Wenn eine Schaltfläche keinen Text anzeigt, muss Ihre Anwendung <a href="tbn-getinfotip.md">normalerweise TBN_GETINFOTIP</a> oder <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> verarbeiten, um eine QuickInfo anzuzeigen. Mit dem TBSTYLE_EX_MIXEDBUTTONS erweiterten Stils wird Text, der zwar festgelegt, aber nicht auf einer Schaltfläche angezeigt wird, automatisch als QuickInfo-Text der Schaltfläche verwendet. Ihre Anwendung muss nur TBN_GETINFOTIP oder oder TTN_GETDISPINFO verarbeiten, wenn sie mehr Flexibilität beim Angeben des QuickInfo-Texts benötigt. <br /> | 
| <span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt></dl> | <a href="common-control-versions.md">Version 5.82</a>. <strong>Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen.</strong> Dieser Stil gibt der Symbolleiste eine vertikale Ausrichtung und organisiert die Symbolleistenschaltflächen in Spalten. Die Schaltflächen fließen vertikal nach unten, bis eine Schaltfläche die begrenzungshöhe der Symbolleiste überschritten hat (siehe <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), und dann wird eine neue Spalte erstellt. Die Symbolleiste durchläuft die Schaltflächen auf diese Weise, bis alle Schaltflächen positioniert sind. Um diesen Stil zu verwenden, muss auch der TBSTYLE_EX_VERTICAL Stil festgelegt werden. <br /><blockquote>[!Note]<br />Dieser Stil wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht unterstützt. Außerdem ist dieser Stil in commctrl.h nicht definiert. Fügen Sie den Quelldateien Ihrer Anwendung die folgende Definition hinzu, um diesen Stil zu verwenden: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code></blockquote><br /> | 
| <span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Version 5.82</a>. <strong>Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen.</strong> Dieser Stil gibt der Symbolleiste eine vertikale Ausrichtung. Symbolleistenschaltflächen werden von oben nach unten anstatt horizontal fließen. <br /><blockquote>[!Note]<br />Dieser Stil wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht unterstützt. Außerdem ist dieser Stil in commctrl.h nicht definiert. Fügen Sie den Quelldateien Ihrer Anwendung die folgende Definition hinzu, um diesen Stil zu verwenden: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code></blockquote><br /> | 




## <a name="remarks"></a>Hinweise

Um einen erweiterten Stil festzulegen, senden Sie dem Symbolleistensteuerelement eine [**TB \_ SETEXTENDEDSTYLE-Meldung.**](tb-setextendedstyle.md) Um zu bestimmen, welche erweiterten Stile derzeit festgelegt sind, senden Sie eine [**\_ TB GETEXTENDEDSTYLE-Nachricht.**](tb-getextendedstyle.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





