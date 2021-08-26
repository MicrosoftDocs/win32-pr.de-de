---
title: Menüleiste (MSAA UI-Elementreferenz)
description: Eine Menüleiste ist der Bereich eines Fensters direkt unter der Titelleiste, der Menüelemente wie Datei, Bearbeiten, Fenster und Hilfe enthält.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1212ba3c56673ab638e5aeedcc0ce20aea68dda2ad55e0904906d9f809c234ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998410"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Menüleiste (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Menüleistenobjekte** für die MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Menüleistenobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Eine Menüleiste ist der Bereich eines Fensters direkt unterhalb der Titelleiste, der Menüelemente wie **Datei,** **Bearbeiten,** **Fenster** und **Hilfe** enthält. Microsoft Active Accessibility erstellt auch ein Menüleistenobjekt für ein Systemmenü, das das Menü in der oberen linken Ecke der Titelleiste darstellt und Menüelemente wie **Wiederherstellen,** **Verschieben,** **Größe,** **Minimieren** und **Maximieren** enthält.

> [!Note]  
> Da Menüleistensteuerelemente keinen Fokus erhalten, werden die [**accSelect-**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) und [**\_ get accFocus-Methoden**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) für dieses Steuerelement nicht unterstützt.

 

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Menüleistensteuerelemente unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Menüleisten-Steuerelemente unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Ruft den [**IDispatch**](idispatch-interface.md) für das angegebene Menüelement ab. Die untergeordneten IDs für die Menüelemente werden sequenziell von links nach rechts nummeriert, beginnend mit 1.                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist die Anzahl der Menüelemente auf der Menüleiste. Die **ChildCount-Eigenschaft** für ein Systemmenü ist eins.                                                                                                                                                                                                                                                   |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Die **Description-Eigenschaft** für eine Menüleiste lautet "Enthält Befehle zum Bearbeiten der aktuellen Ansicht oder des aktuellen Dokuments". Die **Description-Eigenschaft** für ein Systemmenü lautet "Enthält Befehle zum Bearbeiten des Fensters".                                                                                                                                                                   |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** für eine Menüleiste unter der Titelleiste ist "ALT". Die **KeyboardShortcut-Eigenschaft** für ein Systemmenü lautet "ALT+LEERTASTE".                                                                                                                                                                                                                             |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** für eine Menüleiste unter der Titelleiste lautet "Anwendung". Die **Name-Eigenschaft** für ein Systemmenü lautet "System".                                                                                                                                                                                                                                                |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ MENUBAR.**](object-roles.md)                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus einem oder mehreren der folgenden [Werte:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Hinweise

Das System löst mehr als ein [**\_ EREIGNISSYSTEM \_ MENUSTART-Ereignis**](event-constants.md) aus, das nicht immer über ein entsprechendes [**EVENT SYSTEM \_ \_ MENUEND-Ereignis**](event-constants.md) verfügt. Darüber hinaus löst das System die Ereignisse [**EVENT \_ SYSTEM \_ MENUPOPUPSTART**](event-constants.md) und [**EVENT SYSTEM \_ \_ MENUPOPUPEND**](event-constants.md) nicht konsistent aus. Dies ist ein bekanntes Problem, das behoben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Menüelement**](menu-item.md)
</dt> <dt>

[**Popupmenü**](pop-up-menu.md)
</dt> </dl>

 

 





