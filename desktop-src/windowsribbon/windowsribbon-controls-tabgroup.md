---
title: Registerkartengruppe
description: Eine Registerkartengruppe ist ein kontextbezogenes Steuerelement, das zur Laufzeit ausgeblendet oder angezeigt wird, basierend auf einem Dokument- oder Arbeitsbereichszustand. Die Registerkartengruppe enthält eine Reihe kontextbezogener Registerkartensteuerelemente.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ddf1c34903f0660f6f5ead5eb76cd17934ac5cc987358f24c32bc127c73706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117851256"
---
# <a name="tab-group"></a>Registerkartengruppe

Eine Registerkartengruppe ist ein kontextbezogenes Steuerelement, das zur Laufzeit ausgeblendet oder angezeigt wird, basierend auf einem Dokument- oder Arbeitsbereichszustand. Die Registerkartengruppe enthält eine [](windowsribbon-controls-tab.md) Reihe kontextbezogener Registerkartensteuerelemente.

-   [Details](#details)
-   [Registerkartengruppeneigenschaften](#tab-group-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

In der Regel wird eine Registerkartengruppe während bestimmter Dokument- oder Arbeitsbereichszustände angezeigt, z. B. wenn ein Benutzer einen bestimmten Objekttyp auswählt. Für die Auswahl eines Bilds, das im Header einer Tabelle enthalten ist, können beispielsweise verschiedene kontextbezogene Registerkarten angezeigt werden, die sowohl Tabellen- als auch Bildfunktionen verfügbar machen.

> [!IMPORTANT]
> Eine Registerkartengruppe unterstützt keine [Anwendungsmodi.](ribbon-applicationmodes.md) Die einzelnen [Registerkartensteuerelemente](windowsribbon-controls-tab.md) innerhalb einer Registerkartengruppe können jedoch auch sein.

 

Der folgende Screenshot zeigt eine kontextbezogene [Registerkarte](windowsribbon-controls-tab.md) aus Windows 7 Paint.

![Screenshot, der ein kontextbezogenes Registerkartensteuerelement zeigt.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>Registerkartengruppeneigenschaften

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln](windowsribbon-reference-properties.md) für das Registerkartengruppen-Steuerelement.

In der Regel wird eine Registerkartengruppeneigenschaft auf der Menübandbenutzeroberfläche aktualisiert, indem der dem Steuerelement zugeordnete Befehl durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Steuerelement "Registerkartengruppe" zugeordnet sind.



| Eigenschaftenschlüssel                                                                                     | Hinweise                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Ui PKEY ContextAvailable (Benutzeroberflächen-PKEY-Kontext \_ verfügbar)](windowsribbon-reference-properties-uipkey-contextavailable.md)     | Unterstützt [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) |
| [\_PKEY-Keytip der Benutzeroberfläche \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [\_ \_ UI-PKEY-Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                           | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Kann nur durch Ungültigkeit aktualisiert werden.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**TabGroup-Markupelement**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 