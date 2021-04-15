---
title: Menüleiste (MSAA UI-Element Referenz)
description: Eine Menüleiste ist der Bereich eines Fensters direkt unterhalb der Titelleiste, die Menü Elemente enthält, z. b. Datei, bearbeiten, Fenster und Hilfe.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a239a0bb5f860132ba0f9b9393129c2c7a093dae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515764"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Menüleiste (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden **Menü** leisten Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Das Erstellen von **Menü** leisten Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Eine Menüleiste ist der Bereich eines Fensters direkt unterhalb der Titelleiste, die Menü Elemente enthält, z. b. **Datei**, **Bearbeiten**, **Fenster** und **Hilfe**. Microsoft Active Accessibility erstellt außerdem ein Menüleisten Objekt für ein Systemmenü, das das Menü in der oberen linken Ecke der Titelleiste darstellt und Menü Elemente wie **Wiederherstellung**, **verschieben**, **Größe**, **minimieren** und **maximieren** enthält.

> [!Note]  
> Da Menüleisten-Steuerelemente keinen Fokus erhalten, werden die [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) -und [**get- \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) -Methoden für dieses Steuerelement nicht unterstützt.

 

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Menüleisten-Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Menüleisten-Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Ruft das [**IDispatch**](idispatch-interface.md) für das angegebene Menü Element ab. Die untergeordneten IDs für die Menü Elemente werden sequenziell von links nach rechts nummeriert, beginnend mit einem.                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist die Anzahl der Menü Elemente in der Menüleiste. Die **childCount** -Eigenschaft für ein Systemmenü ist 1.                                                                                                                                                                                                                                                   |
| [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Die **Description** -Eigenschaft für eine Menüleiste ist "enthält Befehle zum Bearbeiten der aktuellen Ansicht oder des aktuellen Dokuments". Die **Description** -Eigenschaft für ein Systemmenü ist "enthält Befehle zum Bearbeiten des Fensters".                                                                                                                                                                   |
| [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut** -Eigenschaft für eine Menüleiste unterhalb der Titelleiste ist "alt". Die **KeyboardShortcut** -Eigenschaft für ein Systemmenü ist "Alt + Leertaste".                                                                                                                                                                                                                             |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft für eine Menüleiste unterhalb der Titelleiste lautet "Anwendung". Die **Name** -Eigenschaft für ein Systemmenü ist "System".                                                                                                                                                                                                                                                |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist [**Rollen \_ System- \_ Menüleiste**](object-roles.md).                                                                                                                                                                                                                                                                                      |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System-System eigenes Zustands [**\_ \_**](object-state-constants.md) System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notizen

Das System löst mehr als ein [**\_ \_ MenuStart**](event-constants.md) -Ereignis für das Ereignis System aus, das nicht immer über ein entsprechendes [**Ereignis \_ System- \_ MenuEnd**](event-constants.md) -Ereignis verfügt. Darüber hinaus löst das System das [**Ereignis System " \_ \_ menupopupstart**](event-constants.md) " und das [**Ereignis \_ System " \_ menupopupend**](event-constants.md) " nicht konsistent aus. Dies ist ein bekanntes Problem und wird behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Menü Element**](menu-item.md)
</dt> <dt>

[**Popup Menü**](pop-up-menu.md)
</dt> </dl>

 

 





