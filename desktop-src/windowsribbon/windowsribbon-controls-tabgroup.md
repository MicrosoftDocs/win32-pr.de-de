---
title: Registerkarten Gruppe
description: Eine Registerkarten Gruppe ist ein kontextbezogenes Steuerelement, das zur Laufzeit auf Grundlage eines Dokument-oder Arbeitsbereichs Zustands ausgeblendet oder angezeigt wird. Die Registerkarten Gruppe enthält einen Satz kontextbezogener Registerkarten-Steuerelemente.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316010"
---
# <a name="tab-group"></a>Registerkarten Gruppe

Eine Registerkarten Gruppe ist ein kontextbezogenes Steuerelement, das zur Laufzeit auf Grundlage eines Dokument-oder Arbeitsbereichs Zustands ausgeblendet oder angezeigt wird. Die Registerkarten Gruppe enthält einen Satz kontextbezogener [Register](windowsribbon-controls-tab.md) Karten-Steuerelemente.

-   [Details](#details)
-   [Registerkarten Gruppen Eigenschaften](#tab-group-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

In der Regel wird eine Registerkarten Gruppe in bestimmten Dokument-oder Arbeitsbereichs Zuständen angezeigt, z. b. Wenn ein Benutzer einen bestimmten Objekttyp auswählt. Die Auswahl eines Bilds, das im Header einer Tabelle enthalten ist, kann z. b. erfordern, dass verschiedene Kontext Registerkarten angezeigt werden, die sowohl die Tabellen-als auch die Bild Funktionalität verfügbar machen

> [!IMPORTANT]
> Eine Registerkarten Gruppe unterstützt keine [Anwendungsmodi](ribbon-applicationmodes.md). Allerdings können die einzelnen [Register](windowsribbon-controls-tab.md) Karten-Steuerelemente in einer Registerkarten Gruppe angezeigt werden.

 

Der folgende Screenshot zeigt eine Kontext [Registerkarte](windowsribbon-controls-tab.md) aus Windows 7 Paint.

![Screenshot, der ein Kontext abhängiges Registerkarten-Steuerelement anzeigt.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>Registerkarten Gruppen Eigenschaften

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Registerkarten Gruppen-Steuerelement.

In der Regel wird eine Registerkarten-Gruppen Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle werden die Eigenschaften Schlüssel aufgelistet, die dem Registerkarten-Gruppen Steuerelement zugeordnet sind.



| Eigenschafts Schlüssel                                                                                     | Notizen                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI \_ pkey \_ contextavailable](windowsribbon-reference-properties-uipkey-contextavailable.md)     | Unterstützt [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**iuiframework:: abtuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [UI- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md)                         | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                           | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ tooltipdescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |
| [UI- \_ pkey- \_ ToolTipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**TabGroup-Markup Element**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 