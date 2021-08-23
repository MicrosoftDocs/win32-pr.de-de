---
title: Client-Objekt (MSAA UI-Elementreferenz)
description: Der Clientbereich ist der Teil eines Fensters, in dem die Anwendung Ausgaben wie Text oder Grafiken anzeigt. Beispielsweise zeigt eine Desktopveröffentlichungsanwendung die aktuelle Seite eines Dokuments im Clientbereich an.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33190ebd1013c92a58ecc64b07993a5a5ae1cd842e50c88691295114a128074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645060"
---
# <a name="client-object-msaa-ui-element-reference"></a>Client-Objekt (MSAA UI-Elementreferenz)

Der Clientbereich ist der Teil eines Fensters, in dem die Anwendung Ausgaben wie Text oder Grafiken anzeigt. Beispielsweise zeigt eine Desktopveröffentlichungsanwendung die aktuelle Seite eines Dokuments im Clientbereich an.

Entwickler von Serveranwendungen sind dafür verantwortlich, barrierefreie Objekte zu erstellen, die Informationen zum Inhalt des Clientbereichs der Anwendung bereitstellen.

Wenn eine Clientanwendung Informationen zu einem benutzerdefinierten Benutzeroberflächenelement innerhalb einer Anwendung und zum benutzerdefinierten Benutzeroberflächenelement anfordert, das die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nicht unterstützt, erstellt Microsoft Active Accessibility ein standardmäßig zugängliches Objekt mit minimalen Informationen.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Der Clientbereich unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Der Clientbereich unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Sendet die [**WM \_ GETTEXT-Nachricht,**](/windows/desktop/winmsg/wm-gettext) um den Fenstertext abzurufen.                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ CLIENT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus einem oder mehreren der folgenden [Werte:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

