---
title: ToolTip-Steuer Element (MSAA UI-Element Referenz)
description: Ein QuickInfo-Steuerelement zeigt ein kleines Popup Fenster an, das eine Textzeile enthält, in der der Zweck eines als grafisches Objekt dargestellten Tools in einer Anwendung beschrieben wird.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856160"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a>ToolTip-Steuer Element (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden QuickInfo- **Steuer** Elemente für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Das Erstellen von QuickInfo- **Steuer** Element Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein QuickInfo-Steuerelement zeigt ein kleines Popup Fenster an, das eine Textzeile enthält, in der der Zweck eines als grafisches Objekt dargestellten Tools in einer Anwendung beschrieben wird.

Der Fenster Klassenname für eine QuickInfo ist die Tooltips- \_ Klasse, die als "Tooltips- \_ Klasse" in "kommctrl. h" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein QuickInfo-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein QuickInfo-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Die **childCount** -Eigenschaft ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | Die **Name** -Eigenschaft ist der Text, der im QuickInfo-Steuerelement enthalten ist.                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                               |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | Die **Role** -Eigenschaft [**ist \_ Rollen \_ System**](object-roles.md)-QuickInfo.                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





