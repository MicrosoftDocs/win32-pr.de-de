---
title: Calendar-Steuerelement (REFERENZ ZUM MSAA-UI-Element)
description: Kalendersteuerelemente bieten einem Benutzer eine einfache und intuitive Möglichkeit, ein Datum über eine vertraute Benutzeroberfläche auszuwählen.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f41daf9e86f178f4b22a7908e4d9d10d1dab1a2f867ca2d09c62d111cbc806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899554"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Calendar-Steuerelement (REFERENZ ZUM MSAA-UI-Element)

> [!Note]  
> In diesem Thema werden **Calendar Control-Objekte** für die MsAA-Benutzeroberflächenelementreferenz beschrieben. Das Erstellen von **Calendar Control-Objekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenzdokumentation für das benutzeroberflächenframework, das Sie verwenden.

 

Kalendersteuerelemente bieten einem Benutzer eine einfache und intuitive Möglichkeit, ein Datum über eine vertraute Benutzeroberfläche auszuwählen.

Der Fensterklassenname für ein Monatskalender-Steuerelement ist MONTHCAL CLASS, die \_ in Commctrl.h als "SysMonthCal32" definiert ist. Die Informationen in diesem Thema gelten für das Monatskalender-Steuerelement in Version 5 von Commctrl.h.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Kalendersteuerelemente unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Kalendersteuerelemente unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **ChildCount-Eigenschaft** ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name-Eigenschaft** wird aus dem statischen Textsteuerfeld erhalten, das das Kalendersteuerfeld bezeichnet. Beim Erstellen von Steuerelementen müssen Serverentwickler sicherstellen, dass ein statisches Textsteuerfeld unmittelbar vor dem Steuerelement ausgeführt wird, das in der Registerkartenfolge bezeichnet wird.                                                                                                                                                                                                                 |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das -Steuerelement verfügt.                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ CLIENT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State-Eigenschaft** ist eine Kombination aus [](object-state-constants.md)mindestens einem der folgenden Werte [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





