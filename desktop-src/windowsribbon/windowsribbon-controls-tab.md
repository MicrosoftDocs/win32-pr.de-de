---
title: Registerkarte (Windows Menübandframework)
description: Eine Registerkarte enthält Gruppen verwandter Steuerelemente.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fae518c29e91dac8518c6dc217228e23d0521a562043849f8352783e26e5855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592174"
---
# <a name="tab-windows-ribbon-framework"></a>Registerkarte (Windows Menübandframework)

Eine Registerkarte enthält [Gruppen](windowsribbon-controls-group.md) verwandter Steuerelemente.

-   [Details](#details)
-   [Registerkarteneigenschaften](#tab-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Es gibt drei Arten von Registerkarten im Menübandframework.



| Typ               | Beschreibung                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Registerkarte "Kern"**       | Kernregisterkarten, die die Standardfunktionen der Anwendung organisieren.                                                                                                                                                                                                                   |
| **Registerkarte "Kontext"** | Registerkarten, die während bestimmter Dokument- oder Arbeitsbereichszustände angezeigt werden. Wenn ein Benutzer beispielsweise einen bestimmten Objekttyp auswählt, z. B. ein Bild, das in der Kopfzeile einer Tabelle enthalten ist, werden möglicherweise verschiedene kontextbezogene Registerkarten angezeigt, die sowohl Tabellen- als auch Bildfunktionen verfügbar machen. |
| **Modale Registerkarte**      | Kernregisterkarten, die während eines bestimmten Dokuments oder [Arbeitsbereichs im Anwendungsmodus](ribbon-applicationmodes.md)angezeigt werden, z. B. Die Seitenansicht.                                                                                                                                        |



 

Der folgende Screenshot zeigt eine Kernregisterkarte aus Windows 7 Paint.

![Screenshot, der ein Kernregisterkarten-Steuerelement zeigt.](images/controls/coretab.png)

## <a name="tab-properties"></a>Registerkarteneigenschaften

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln](windowsribbon-reference-properties.md) für das Registerkarten-Steuerelement.

In der Regel wird eine Tab-Eigenschaft auf der Menübandbenutzeroberfläche aktualisiert, indem der dem Steuerelement zugeordnete Befehl durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Registerkartensteuerelement zugeordnet sind.



| Eigenschaftenschlüssel                                                                                     | Hinweise                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [\_ \_ UI-PKEY-Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                           | Kann nur durch Ungültigkeit aktualisiert werden. |
| [\_PKEY-Keytip der Benutzeroberfläche \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Kann nur durch Ungültigkeit aktualisiert werden. |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Kann nur durch Ungültigkeit aktualisiert werden. |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Kann nur durch Ungültigkeit aktualisiert werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Registerkartenmarkupelement**](windowsribbon-element-tab.md)
</dt> </dl>

 

 
