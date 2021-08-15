---
title: MDI-Clientfenster (REFERENZ ZUM MSAA-UI-Element)
description: Die MDI (Multiple Document Interface) ist eine Spezifikation, die die Standard-Benutzeroberfläche für Anwendungen definiert, die für Windows. Eine MDI-Anwendung ermöglicht es einem Benutzer, mit mehr als einem Dokument gleichzeitig zu arbeiten.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff8279e9934c953e30a7d91710565562cb538d3140d971b1f74ff8963ca7345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565131"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>MDI-Clientfenster (REFERENZ ZUM MSAA-UI-Element)

Die MDI (Multiple Document Interface) ist eine Spezifikation, die die Standard-Benutzeroberfläche für Anwendungen definiert, die für Windows. Eine MDI-Anwendung ermöglicht es einem Benutzer, mit mehr als einem Dokument gleichzeitig zu arbeiten.

Eine MDI-Anwendung verfügt über drei Arten von Fenstern: ein Rahmenfenster, ein Clientfenster und eine Reihe untergeordneter Fenster. Das Rahmenfenster ist wie das Hauptfenster einer Anwendung und umschließt das Clientfenster. Das Clientfenster ist ein untergeordnetes Fenster des Rahmenfensters und dient als Hintergrund für die untergeordneten Fenster. Das Clientfenster bietet auch Unterstützung für das Erstellen und Bearbeiten der untergeordneten Fenster, in denen Dokumente angezeigt werden.

Der Fensterklassenname für ein MDI-Clientfenster ist "MDIClient".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein MDI-Clientfenster unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein MDI-Clientfenster unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **ChildCount-Eigenschaft** gibt die Anzahl der untergeordneten Fenster an, in denen Dokumente angezeigt werden.                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name-Eigenschaft** ist "Workspace".                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die **Parent-Eigenschaft** ist das MDI-Rahmenfenster.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ CLIENT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State-Eigenschaft** ist eine Kombination aus mindestens einem der folgenden [Werte:](object-state-constants.md)STATE [**SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





