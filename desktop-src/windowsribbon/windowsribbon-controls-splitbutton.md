---
title: Unterteilte Schaltfläche
description: Die Schaltfläche Teilen ist ein zusammengesetztes Steuerelement, mit dem der Benutzer einen Standardwert auswählen kann, der an eine primäre Schaltfläche gebunden ist, oder aus einer Liste von sich gegenseitig ausschließenden Werten auswählen kann, die in einer Dropdownliste angezeigt werden, die an eine sekundäre Schaltfläche gebunden ist.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5d9554af8c580b5288a2f18eaef89a1d7e864bae628ebac59599f6b7f820f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202491"
---
# <a name="split-button"></a>Unterteilte Schaltfläche

Die Schaltfläche Teilen ist ein zusammengesetztes Steuerelement, mit dem der Benutzer einen Standardwert auswählen kann, der an eine primäre Schaltfläche gebunden ist, oder aus einer Liste von sich gegenseitig ausschließenden Werten auswählen kann, die in einer Dropdownliste angezeigt werden, die an eine sekundäre Schaltfläche gebunden ist.

-   [Introduction (Einführung)](#introduction)
-   [Eigenschaften der geteilten Schaltfläche](#split-button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Dieses Steuerelement ist nützlich, um eng verwandte Elemente in Fällen verfügbar zu machen, in denen ein offensichtlicher Standardwert verfügbar ist und die einzelnen Elemente durch ein Bild, Text oder beides dargestellt werden können.

Der folgende Screenshot veranschaulicht die Schaltfläche zum Teilen des Menübands.

![Screenshot eines Splitbutton-Steuerelements in einem Beispielband.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Eigenschaften der geteilten Schaltfläche

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln für](windowsribbon-reference-properties.md) das Split Button-Steuerelement.

In der Regel wird eine Split Button-Eigenschaft in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Steuerelement Schaltfläche teilen zugeordnet sind.



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
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a><br/> Wenn alle untergeordneten Elemente deaktiviert sind, legt das Framework <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> false (0) fest. Wenn ein oder mehrere untergeordnete Elemente aktiviert sind, wird UI_PKEY_Enabled auf true (-1) festgelegt.
<blockquote>
[!Important]<br />
Die <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled-Eigenschaft</a> für das Split Button-Steuerelement sollte ungültig gemacht werden, nachdem mindestens ein untergeordnetes Objekt aktiviert oder deaktiviert wurde. Dadurch wird sichergestellt, dass das Framework den aktualisierten Eigenschaftswert abfragt und den Zustand des Split Button-Steuerelements in der Menübandbenutzeroberfläche aktualisiert.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**SplitButton-Markupelement**](windowsribbon-element-splitbutton.md)
</dt> </dl>