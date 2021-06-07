---
title: Switch-Fenster (MSAA UI-Elementreferenz)
description: Das Schalterfenster wird angezeigt, wenn ein Benutzer ALT+TAB drückt, um zu einer anderen Anwendung zu wechseln. Das Switchfenster enthält ein Symbol für jede derzeit ausgeführte Anwendung.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443981"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Switch-Fenster (MSAA UI-Elementreferenz)

Das Schalterfenster wird angezeigt, wenn ein Benutzer ALT+TAB drückt, um zu einer anderen Anwendung zu wechseln. Das Switchfenster enthält ein Symbol für jede derzeit ausgeführte Anwendung.

Der Name der Fensterklasse für das Switchfenster lautet " \# 32771".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Das Switchfenster unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Methode                                                                    | Kommentare                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Das Switchfensterobjekt selbst verfügt nicht über eine **DefaultAction-Eigenschaft.** Die [**accDoDefaultAction-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) für jedes Element im Switchfenster aktiviert das angegebene Element. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Das Schalterfenster unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



|      Eigenschaft                                                                          |      BESCHREIBUNG                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | Die **ChildCount-Eigenschaft** ist 0 (null).                                                                                                                                                                                           |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | Das Switchfensterobjekt selbst verfügt nicht über eine **DefaultAction-Eigenschaft.** Die **DefaultAction-Eigenschaft** für jedes Element im Switchfenster lautet "Switch".                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | Das übergeordnete Objekt des Switchfensters kann den Fokus nicht erhalten. nur die einzelnen untergeordneten Elemente können den Fokus erhalten.                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | Das Switchfensterobjekt selbst verfügt nicht über eine **Name-Eigenschaft.** Die **Name-Eigenschaft** für jedes Anwendungssymbol im Switchfenster entspricht dem angezeigten Anwendungsnamen.                                         |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | Das Switchfensterobjekt selbst verfügt über die **Role-Eigenschaft** "window \[ 32771". \] Außerdem verfügt jedes Anwendungssymbol im Switchfenster über die **Role-Eigenschaft** [**ROLE SYSTEM \_ \_ LISTITEM**](object-roles.md). |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Das Switchfensterobjekt selbst unterstützt die **State-Eigenschaft** nicht. Der **Wert State** für die Listenansichtselemente ist STATE SYSTEM [**\_ \_ FOCUSABLE.**](object-state-constants.md)                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




