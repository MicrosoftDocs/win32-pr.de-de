---
title: Calendar-Steuer Element (MSAA-Benutzeroberflächen Element-Referenz)
description: Kalender Steuerelemente bieten eine einfache und intuitive Möglichkeit für einen Benutzer, ein Datum aus einer vertrauten Oberfläche auszuwählen.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855780"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Calendar-Steuer Element (MSAA-Benutzeroberflächen Element-Referenz)

> [!Note]  
> In diesem Thema werden **Kalender Steuer** Element Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Die Vorgehensweise zum Erstellen von **Kalender Steuer** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Kalender Steuerelemente bieten eine einfache und intuitive Möglichkeit für einen Benutzer, ein Datum aus einer vertrauten Oberfläche auszuwählen.

Der Fenster Klassenname für ein Monatskalender-Steuerelement ist eine monthcal- \_ Klasse, die in "kommctrl. h" als "SysMonthCal32" definiert ist. Die Informationen in diesem Thema gelten für das Month Calendar-Steuerelement in Version 5 von "kommctrl. h".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Kalender Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Kalender Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **childCount** -Eigenschaft ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name** -Eigenschaft wird aus dem statischen Text Steuerelement abgerufen, das das Kalender Steuerelement bezeichnet. Beim Erstellen von Steuerelementen müssen Server Entwickler sicherstellen, dass ein statisches Text Steuerelement unmittelbar vor dem Steuerelement liegt, das es in der Aktivier Reihenfolge bezeichnet                                                                                                                                                                                                                 |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                             |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role** -Eigenschaft ist [**role \_ System \_ Client**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md)[**Zustands \_ System nicht \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





