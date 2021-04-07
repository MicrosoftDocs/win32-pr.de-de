---
title: Gruppenfeld (MSAA UI-Element Referenz)
description: Ein Gruppenfeld ist ein Rechteck, das einen Satz von Steuerelementen umgibt, z. b. Kontrollkästchen oder Options Felder, und einen Anwendungs definierten Text (Bezeichnung) enthält.
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712570"
---
# <a name="group-box-msaa-ui-element-reference"></a>Gruppenfeld (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden **Gruppenfeld** Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Das Erstellen von **Gruppenfeld** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein Gruppenfeld ist ein Rechteck, das einen Satz von Steuerelementen umgibt, z. b. Kontrollkästchen oder Options Felder, und einen Anwendungs definierten Text (Bezeichnung) enthält.

Der einzige Zweck eines Gruppen Felds besteht darin, Steuerelemente zu organisieren, die durch einen gemeinsamen Zweck, angegeben durch die Bezeichnung, verknüpft sind.

Der Fenster Klassenname für ein Gruppenfeld ist "Schaltfläche".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Gruppenfeld unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Gruppenfeld unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist immer 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Gruppen Felder haben keine Tastenkombinationen. Wenn der Fenster Text für das Feld Gruppe jedoch ein kaufmännisches und-Zeichen (&) enthält, gibt Microsoft Active Accessibility eine Zeichenfolge ungleich NULL als **KeyboardShortcut** -Eigenschaft zurück.                                                                                                                                                                                                                                            |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft wird aus dem Fenster Text (oder der Beschriftung) des Steuer Elements abgerufen, der mit dem Gruppenfeld angezeigt wird.                                                                                                                                                                                                                                                                                                                                                    |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                              |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist eine [**Rollen \_ System \_ Gruppierung**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





