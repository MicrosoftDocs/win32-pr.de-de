---
title: Popup Menü (MSAA UI-Element Referenz)
description: In einem Popupmenü wird eine Liste mit Menübefehlen angezeigt.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856496"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Popup Menü (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden **Popup Menü** Objekte zum Zweck der MSAA-Benutzeroberflächen-Element Referenz beschrieben. Hier wird beschrieben, wie Sie **Popup Menü** Objekte in verschiedenen Benutzeroberflächen-Frameworks erstellen. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

In einem Popupmenü wird eine Liste mit Menübefehlen angezeigt. Microsoft Active Accessibility erstellt ein Popup-Menü Objekt, wenn ein Menü Element in einer Menüleiste geöffnet wird. Microsoft Active Accessibility erstellt auch Menü-Popup Objekte für Kontextmenüs, die angezeigt werden, wenn der Benutzer mit der rechten Maustaste auf ein Benutzeroberflächen Element klickt.

Der Fenster Klassenname für ein Popup Menü ist " \# 32768".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Popup Menü unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Popup Menü unterstützt [**die folgenden Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , auf die zugegriffen werden kann:



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Ruft das [**IDispatch**](idispatch-interface.md) für das angegebene Menü Element ab. Die untergeordneten IDs für die Menü Elemente werden nacheinander von oben nach unten nummeriert, beginnend mit einem.                                                                                                                                                                                                                                                                                      |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **childCount** -Eigenschaft ist die Anzahl der Menü Elemente im Menü, einschließlich Menü Trennzeichen.                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name** -Eigenschaft für ein Popup Menü ist derselbe Name wie das Menü. Die **Name** -Eigenschaft für ein Kontextmenü ist "Context".                                                                                                                                                                                                                                                                                                                                              |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Popup Menü umgibt und die **Name** -Eigenschaft und den Namen der Fenster Klasse wie das Popup Menü enthält.                                                                                                                                                                                                                                                      |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role** -Eigenschaft ist [**Rollen \_ System- \_ menupup**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notizen

-   Popup-Menü Objekte erzeugen keine Ereignisse für [**Ereignis \_ Objekt \_ Erstellung**](event-constants.md) und [**Ereignis \_ Objekt \_ Zerstörung**](event-constants.md) .
-   Mehrspaltige Menüs unterstützen nicht die Rechte des [**navDir \_ left**](navigation-constants.md) -oder [**\_ navDir**](navigation-constants.md) -Flags der [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) -Methode.
-   Das [**Ereignis \_ System " \_ menupopupstart**](event-constants.md) " und das [**Ereignis \_ System " \_ menupopupend**](event-constants.md) " werden nicht konsistent gesendet. Dies ist ein bekanntes Problem und wird behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Menüleiste**](menu-bar.md)
</dt> <dt>

[**Menü Element**](menu-item.md)
</dt> </dl>

 

 





