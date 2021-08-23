---
title: Headersteuerelement (MSAA UI-Elementreferenz)
description: Ein Headersteuerelement zeigt Überschriften am oberen Rand der Informationsspalten an und ermöglicht es dem Benutzer, die Informationen durch Klicken auf die Überschriften zu sortieren. Windows Der Explorer verwendet ein Headersteuerelement, wenn die Detailansicht ausgewählt ist.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c378bb0244e94f4cb95c8b2ba90512d2b17542bdef7428197ee58479dbfde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994180"
---
# <a name="header-control-msaa-ui-element-reference"></a>Headersteuerelement (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Header Control-Objekte** für die MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Headersteuerelementobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Ein Headersteuerelement zeigt Überschriften am oberen Rand der Informationsspalten an und ermöglicht es dem Benutzer, die Informationen durch Klicken auf die Überschriften zu sortieren. Windows Der Explorer verwendet ein Headersteuerelement, wenn die Detailansicht ausgewählt ist.

Der Fensterklassenname für ein Headersteuerelement ist WC \_ HEADER, der in Commctrl.h als "SysHeader32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Headersteuerelement unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Methode                                                                    | Kommentare                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Diese Methode führt die Standardaktion durch Klicken auf den Header aus. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Headersteuerelement unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                       | Kommentare                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | Die **ChildCount-Eigenschaft** ist 0 (null).                                                                                                                                                                                                   |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | Die **DefaultAction-Eigenschaft** ist "Click".                                                                                                                                                                                             |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | Die **Name-Eigenschaft** entspricht dem Namen der Spaltenüberschrift.                                                                                                                                                                    |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ LIST**](object-roles.md) ), das das Steuerelement umgibt und den gleichen Fensterklassennamen wie das Steuerelement hat.                                                      |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ COLUMNHEADER.**](object-roles.md)                                                                                                                                  |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Der Wert für die **State-Eigenschaft** ist immer [**STATE SYSTEM \_ \_ READONLY**](object-state-constants.md) und kann auch [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md)enthalten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




