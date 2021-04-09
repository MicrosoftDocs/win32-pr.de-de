---
title: Client Objekt (MSAA UI-Element Referenz)
description: Der Client Bereich ist der Teil eines Fensters, in dem die Anwendung Ausgaben anzeigt, z. b. Text oder Grafiken. Beispielsweise zeigt eine Desktop Publishing Anwendung die aktuelle Seite eines Dokuments im Client Bereich an.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be28ae4c31e1a2d2f72674a39d7db08730562816
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101882"
---
# <a name="client-object-msaa-ui-element-reference"></a>Client Objekt (MSAA UI-Element Referenz)

Der Client Bereich ist der Teil eines Fensters, in dem die Anwendung Ausgaben anzeigt, z. b. Text oder Grafiken. Beispielsweise zeigt eine Desktop Publishing Anwendung die aktuelle Seite eines Dokuments im Client Bereich an.

Entwickler von Server Anwendungen sind dafür verantwortlich, barrierefreie Objekte zu erstellen, die Informationen über den Inhalt des Client Bereichs der Anwendung bereitstellen.

Wenn eine Client Anwendung Informationen zu einem benutzerdefinierten Benutzeroberflächen Element innerhalb einer Anwendung anfordert und das benutzerdefinierte UI-Element, das die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle nicht unterstützt, erstellt Microsoft Active Accessibility ein barrierefreies Standard Objekt mit minimalen Informationen.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Der-Client Bereich unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Der Client Bereich unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Sendet die [**WM- \_ gettext**](/windows/desktop/winmsg/wm-gettext) -Nachricht, um den Fenster Text abzurufen.                                                                                                                                                                                                                                                                                                                                                                                |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist [**role \_ System \_ Client**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

