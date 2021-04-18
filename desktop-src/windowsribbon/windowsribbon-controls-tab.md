---
title: Registerkarte (Windows-Menü Band Framework)
description: Eine Registerkarte enthält Gruppen von verknüpften Steuerelementen.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340248"
---
# <a name="tab-windows-ribbon-framework"></a>Registerkarte (Windows-Menü Band Framework)

Eine Registerkarte enthält [Gruppen](windowsribbon-controls-group.md) von verknüpften Steuerelementen.

-   [Details](#details)
-   [Registerkarteneigenschaften](#tab-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Es gibt drei Arten von Registerkarten im Menüband-Framework.



| type               | BESCHREIBUNG                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kern Registerkarte**       | Kern Registerkarten, die die Standardfunktionen der Anwendung organisieren.                                                                                                                                                                                                                   |
| **Kontext Registerkarte** | Registerkarten, die in bestimmten Dokument-oder Arbeitsbereichs Zuständen angezeigt werden. Wenn ein Benutzer beispielsweise einen bestimmten Objekttyp auswählt, z. b. ein Bild, das im Header einer Tabelle enthalten ist, werden möglicherweise verschiedene Kontext Registerkarten angezeigt, die sowohl die Tabellen-als auch die Bild Funktionalität verfügbar machen. |
| **Modale Registerkarte**      | Kern Registerkarten, die in einem bestimmten Dokument-oder Arbeitsbereichs [Anwendungsmodus](ribbon-applicationmodes.md)angezeigt werden, z. b. in der Druckvorschau.                                                                                                                                        |



 

Der folgende Screenshot zeigt eine Kern Registerkarte aus Windows 7 Paint.

![Screenshot mit einem Registerkarten-Steuerelement.](images/controls/coretab.png)

## <a name="tab-properties"></a>Registerkarteneigenschaften

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Registerkarten-Steuerelement.

In der Regel wird eine Registerkarten Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Registerkarten-Steuerelement zugeordnet sind.



| Eigenschafts Schlüssel                                                                                     | Notizen                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)                           | Kann nur durch Invalidierung aktualisiert werden. |
| [UI- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md)                         | Kann nur durch Invalidierung aktualisiert werden. |
| [UI- \_ pkey- \_ tooltipdescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Kann nur durch Invalidierung aktualisiert werden. |
| [UI- \_ pkey- \_ ToolTipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Kann nur durch Invalidierung aktualisiert werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Tab-Markup Element**](windowsribbon-element-tab.md)
</dt> </dl>

 

 
