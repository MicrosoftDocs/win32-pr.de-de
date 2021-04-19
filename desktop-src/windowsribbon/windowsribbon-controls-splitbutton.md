---
title: Unterteilte Schaltfläche
description: Die unterteilte Schaltfläche ist ein zusammengesetztes Steuerelement, mit dem der Benutzer einen Standardwert auswählen kann, der an eine primär Schaltfläche gebunden ist, oder aus einer Liste von sich gegenseitig ausschließenden Werten auswählen, die in einer Dropdown Liste an eine sekundäre Schaltfläche
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106341565"
---
# <a name="split-button"></a>Unterteilte Schaltfläche

Die unterteilte Schaltfläche ist ein zusammengesetztes Steuerelement, mit dem der Benutzer einen Standardwert auswählen kann, der an eine primär Schaltfläche gebunden ist, oder aus einer Liste von sich gegenseitig ausschließenden Werten auswählen, die in einer Dropdown Liste an eine sekundäre Schaltfläche

-   [Introduction (Einführung)](#introduction)
-   [Eigenschaften für getrennte Schaltflächen](#split-button-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Dieses Steuerelement ist nützlich, um eng verwandte Elemente in Fällen verfügbar zu machen, in denen ein offensichtlicher Standard verfügbar ist und die einzelnen Elemente durch ein Bild, Text oder beides dargestellt werden können.

Der folgende Screenshot veranschaulicht die unterteilte Schaltfläche des Menübands.

![Screenshot eines SplitButton-Steuer Elements in einem beispielmenüband.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Eigenschaften für getrennte Schaltflächen

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Steuerelement unterteilte Schaltflächen.

In der Regel wird eine unterteilte Schaltflächen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Steuerelement für die unterteilte Schaltfläche zugeordnet sind.



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
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.<br/> Wenn alle untergeordneten Elemente deaktiviert sind, legt das Framework <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> auf false (0) fest. Wenn ein oder mehrere untergeordnete Elemente aktiviert sind, wird UI_PKEY_Enabled auf true (-1) festgelegt.
<blockquote>
[!Important]<br />
Die <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> -Eigenschaft für das Steuerelement für die unterteilte Schaltfläche sollte ungültig werden, nachdem mindestens ein untergeordnetes Element aktiviert oder deaktiviert wurde. Dadurch wird sichergestellt, dass das Framework den aktualisierten Eigenschafts Wert abfragt und den Zustand des Steuer Elements unterteilte Schaltflächen auf der Multifunktionsleisten-Benutzeroberfläche aktualisiert.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
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

[**SplitButton-Markup Element**](windowsribbon-element-splitbutton.md)
</dt> </dl>