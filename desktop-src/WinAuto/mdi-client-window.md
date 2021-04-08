---
title: MDI-Client Fenster (MSAA UI-Element Referenz)
description: Die Multiple Document Interface (MDI) ist eine Spezifikation, die die Standardbenutzer Oberfläche für für Windows geschriebene Anwendungen definiert. Mithilfe einer MDI-Anwendung kann ein Benutzer mehrere Dokumente gleichzeitig bearbeiten.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947672"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>MDI-Client Fenster (MSAA UI-Element Referenz)

Die Multiple Document Interface (MDI) ist eine Spezifikation, die die Standardbenutzer Oberfläche für für Windows geschriebene Anwendungen definiert. Mithilfe einer MDI-Anwendung kann ein Benutzer mehrere Dokumente gleichzeitig bearbeiten.

Eine MDI-Anwendung verfügt über drei Arten von Fenstern: ein Rahmen Fenster, ein Client Fenster und eine Reihe von untergeordneten Fenstern. Das Rahmen Fenster ist wie das Hauptfenster einer Anwendung und umgibt das Client Fenster. Das Client Fenster ist ein untergeordnetes Element des Rahmen Fensters und dient als Hintergrund für die untergeordneten Fenster. Das Client Fenster bietet auch Unterstützung für das Erstellen und Bearbeiten der untergeordneten Fenster, in denen Dokumente angezeigt werden.

Der Fenster Klassenname für ein MDI-Client Fenster lautet "MdiClient".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein MDI-Client Fenster unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein MDI-Client Fenster unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **childCount** -Eigenschaft ist die Anzahl der untergeordneten Fenster, in denen Dokumente angezeigt werden.                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name** -Eigenschaft ist "Workspace".                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die über **geordnete** Eigenschaft ist das MDI-Rahmen Fenster.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role** -Eigenschaft ist [**Rollen \_ System \_ Client**](object-roles.md) .                                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_Zugriffs Auswahl**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





