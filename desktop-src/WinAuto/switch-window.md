---
title: Fenster wechseln (MSAA UI-Element Referenz)
description: Das Fenster Switch wird angezeigt, wenn ein Benutzer Alt + Tab drückt, um zu einer anderen Anwendung zu wechseln. Das Fenster Switch enthält ein Symbol für jede Anwendung, die gerade ausgeführt wird.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714129"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Fenster wechseln (MSAA UI-Element Referenz)

Das Fenster Switch wird angezeigt, wenn ein Benutzer Alt + Tab drückt, um zu einer anderen Anwendung zu wechseln. Das Fenster Switch enthält ein Symbol für jede Anwendung, die gerade ausgeführt wird.

Der Fenster Klassenname für das Fenster Switch lautet " \# 32771".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Das Fenster Switch unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:



| Methode                                                                    | Kommentare                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Das Switch Window-Objekt selbst verfügt über keine **DEFAULTACTION** -Eigenschaft. Die [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) -Methode für jedes Element im Switch-Fenster aktiviert das angegebene Element. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Das Fenster Switch unterstützt die [**folgenden Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , auf die zugegriffen werden kann:



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | Die **childCount** -Eigenschaft ist 0 (null).                                                                                                                                                                                           |
| [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | Das Switch Window-Objekt selbst verfügt über keine **DEFAULTACTION** -Eigenschaft. Die **DEFAULTACTION** -Eigenschaft für jedes Element im Switch-Fenster ist "Switch".                                                                     |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | Das übergeordnete Objekt des Switch-Fensters kann den Fokus nicht erhalten. nur die einzelnen untergeordneten Elemente können den Fokus erhalten.                                                                                                                          |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | Das Switch Window-Objekt selbst hat keine **Name** -Eigenschaft. Die **Name** -Eigenschaft für jedes Anwendungssymbol im Fenster Switch ist mit dem angezeigten Anwendungsnamen identisch.                                         |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | Das Switch Window-Objekt selbst verfügt über die **Role** -Eigenschaft "Window \[ 32771 \] ". Außerdem verfügt jedes Anwendungssymbol im Fenster Switch über die **Rollen** Eigenschaften [**Rolle \_ System \_ ListItem**](object-roles.md). |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Das Switch Window-Objekt selbst unterstützt die **State** -Eigenschaft nicht. Der **Zustands** Wert für die Listen Ansichts Elemente ist [**Zustands \_ System- \_ focverwendbar**](object-state-constants.md).                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




