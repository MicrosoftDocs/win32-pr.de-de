---
title: Up-Down-Steuerelement (MSAA UI-Elementreferenz)
description: Ein Auf-Ab-Steuerelement, auch als Drehsteuerelement bezeichnet, kombiniert ein Als Pfeile angezeigtes Schaltflächenpaar mit einem Bearbeitungssteuerelement. Durch Klicken auf die Pfeile wird der Wert im Bearbeitungssteuerelement erhöht oder dekrementiert.
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b9475d8bbca24d2bf536a4eb9a9decf078297e788a37aa4d8560029a67e50e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114625"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Up-Down-Steuerelement (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Up-Down Control-Objekte** für die MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Up-Down-Steuerelementobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Ein Auf-Ab-Steuerelement, auch als Drehsteuerelement bezeichnet, kombiniert ein Als Pfeile angezeigtes Schaltflächenpaar mit einem Bearbeitungssteuerelement. Durch Klicken auf die Pfeile wird der Wert im Bearbeitungssteuerelement erhöht oder dekrementiert.

Der Fensterklassenname für ein Auf-Ab-Steuerelement ist UPDOWN \_ CLASS, die in Commctrl.h als "msctls \_ updown32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Auf-Ab-Steuerelement unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Auf-Ab-Steuerelement unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **ChildCount-Eigenschaft** ist "2" (die Pfeilschaltflächen nach oben und unten).                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name-Eigenschaft** für das Up-Down-Steuerelementobjekt wird aus dem Fenstertext (oder der Beschriftung) des Steuerelements abgerufen. Dieser Text wird nicht mit dem Up-Down-Steuerelement angezeigt, sodass Serverentwickler in der Ressourcendefinitions-Anweisung des Steuerelements aussagekräftigen Text bereitstellen müssen, damit Benutzer von Clienthilfsprogrammen das Steuerelement identifizieren können. Die **Name-Eigenschaft** für die Schaltfläche mit dem oberen Pfeil im Steuerelement nach oben ist "More", und die **Name-Eigenschaft** für die Schaltfläche mit dem unteren Pfeil ist "Less". |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die **Parent-Eigenschaft** des Auf-Ab-Steuerelements ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das Steuerelement verfügt. Die **Parent-Eigenschaft** der Nach-oben- und Nach-unten-Pfeilschaltflächen ist das Up-Down-Steuerelementobjekt.                                                                                                                                                    |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role-Eigenschaft** für das Up-Down-Steuerelementobjekt ist [**ROLE SYSTEM \_ \_ SPINBUTTON.**](object-roles.md) Die **Role-Eigenschaft** für die Pfeilschaltflächen ist [**ROLE SYSTEM \_ \_ PUSHBUTTON.**](object-roles.md)                                                                                                                                                                                                                          |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die State-Eigenschaft für das Up-Down-Steuerelementobjekt ist einer der folgenden [Werte:](object-state-constants.md)[**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/>                                                                                                                                                                                      |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Hinweise

Microsoft Active Accessibility macht das Bearbeitungssteuerelement als separates Objekt verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





