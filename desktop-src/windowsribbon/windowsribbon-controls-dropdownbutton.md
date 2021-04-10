---
title: Drop-Down Schaltfläche
description: Die Schaltfläche "Drop-Down" besteht aus einer Schaltfläche, die beim Klicken auf eine Dropdown Liste mit sich gegenseitig ausschließenden Elementen zeigt.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87e6a776dd705fe503e5e93ec601baf6cc2b3cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316629"
---
# <a name="drop-down-button"></a>Drop-Down Schaltfläche

Die Schaltfläche "Drop-Down" besteht aus einer Schaltfläche, die beim Klicken auf eine Dropdown Liste mit sich gegenseitig ausschließenden Elementen zeigt.

-   [Details](#details)
-   [Eigenschaften der Dropdown Schaltfläche](#drop-down-button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Dieses Steuerelement ist nützlich, um eng verwandte Elemente in Fällen verfügbar zu machen, in denen kein offensichtlicher Standard verfügbar ist und die einzelnen Elemente durch ein Bild, Text oder beides dargestellt werden können.

Der folgende Screenshot veranschaulicht die Menüband-Drop-Down Schaltfläche in einem Beispiel-Menüband.

![Screenshot eines Dropdown Button-Steuer Elements in einem beispielmenüband.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a>Eigenschaften der Drop-Down Schaltfläche

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Drop-Down Button-Steuerelement.

In der Regel wird eine Drop-Down Button-Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Schaltflächen-Steuerelement Drop-Down zugeordnet sind.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschafts Schlüssel</th>
<th>Notizen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.<br/> Wenn alle untergeordneten Elemente deaktiviert sind, legt das Framework <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> auf false (0) fest. Wenn ein oder mehrere untergeordnete Elemente aktiviert sind, wird UI_PKEY_Enabled auf true (-1) festgelegt.
<blockquote>
[!Important]<br />
Die <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> -Eigenschaft für das Drop-Down Button-Steuerelement sollte ungültig werden, nachdem mindestens ein untergeordnetes Element aktiviert oder deaktiviert wurde. Dadurch wird sichergestellt, dass das Framework den aktualisierten Eigenschafts Wert abfragt und den Zustand des Steuer Elements Drop-Down Schaltfläche in der Multifunktionsleisten-Benutzeroberfläche aktualisiert.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.
<blockquote>
[!Note]<br />
Wenn der Befehl, der dem Steuerelement zugeordnet ist, durch einen <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>iuiframework:: invalidateuicommand</strong></a>-Befehl ungültig gemacht wird, fragt das Framework diese Eigenschaft ab, wenn <code>UI_INVALIDATIONS_VALUE</code> als Wert von <em>Flags</em>übergeben wird.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**DropDownButton-Markup Element**](windowsribbon-element-dropdownbutton.md)
</dt> </dl>