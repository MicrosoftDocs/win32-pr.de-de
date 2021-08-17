---
title: Umschaltfläche
description: Wenn Sie auf die Umschaltfläche klicken, wird eine Eingabe für eine Anwendung angezeigt. Das -Steuerelement stellt einen sich gegenseitig ausschließenden Umschaltzustand dar.
ms.assetid: 290052b7-0528-41c5-b6f4-958cc42d502b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd4f9cd407ff8d2a08ca8bc8313f25374a429c1038544f0d31f270621af0267f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964343"
---
# <a name="toggle-button"></a>Umschaltfläche

Wenn Sie auf die Umschaltfläche klicken, wird eine Eingabe für eine Anwendung angezeigt. Das -Steuerelement stellt einen sich gegenseitig ausschließenden Umschaltzustand dar.

-   [Details](#details)
-   [Eigenschaften der Umschaltfläche](#toggle-button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Der folgende Screenshot veranschaulicht die Umschaltfläche des Menübands.

![Screenshot eines Togglebutton-Steuerelements im Microsoft-Farbband.](images/controls/togglebutton.png)

## <a name="toggle-button-properties"></a>Eigenschaften der Umschaltfläche

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln für](windowsribbon-reference-properties.md) das Steuerelement Schaltfläche umschalten.

In der Regel wird eine Umschaltfläche-Eigenschaft in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Steuerelement Schaltfläche umschalten zugeordnet sind.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaftsschlüssel</th>
<th>Hinweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a>
<blockquote>
[!Note]<br />
Wenn der dem Steuerelement zugeordnete Befehl durch einen Aufruf von <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>ungültig gemacht wird, fragt das Framework diese Eigenschaft ab, wenn als Wert von flags übergeben <code>UI_INVALIDATIONS_VALUE</code> <em>wird.</em>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**ToggleButton-Markupelement**](windowsribbon-element-togglebutton.md)
</dt> </dl>

