---
title: Animations Steuer Element (MSAA UI-Element Referenz)
description: Animations Steuerelemente zeigen im Hintergrund einen AVI-Clip (Audiovideo überlappende) an. Animations Steuerelemente werden normalerweise angezeigt, wenn Dateien kopiert werden oder wenn eine andere zeitaufwändige Aufgabe ausgeführt wird.
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ca7cf7e4b8a2174dae81b1770b2d877f749502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710692"
---
# <a name="animation-control-msaa-ui-element-reference"></a>Animations Steuer Element (MSAA UI-Element Referenz)

Animations Steuerelemente zeigen im Hintergrund einen AVI-Clip (Audiovideo überlappende) an. Animations Steuerelemente werden normalerweise angezeigt, wenn Dateien kopiert werden oder wenn eine andere zeitaufwändige Aufgabe ausgeführt wird.

Der Fenster Klassenname für ein Animations Steuerelement ist eine animieren- \_ Klasse, die in "Komma STRG. h" als "SysAnimate32" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Animations Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Animations Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Animations Steuerelemente haben keine Tastenkombinationen. Wenn die Bezeichnung für das Steuerelement jedoch eine Zugriffstaste enthält (ein unterstrichenes Zeichen im Text der Bezeichnung des Steuer Elements), gibt [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) eine Zeichenfolge zurück, die nicht NULL ist. Diese Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird. Wenn die Bezeichnung z. b. "Dateien herunterladen" lautet, lautet **KeyboardShortcut** "alt + d".                                                                                        |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft wird aus dem statischen Text Steuerelement abgerufen, das das Animations Steuerelement bezeichnet. Beim Erstellen von Steuerelementen müssen Server Entwickler sicherstellen, dass ein statisches Text Steuerelement unmittelbar vor dem Steuerelement liegt, das es in der Aktivier Reihenfolge bezeichnet                                                                                                                                                                                                                                                                                             |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                                                                                                          |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist eine [**\_ \_ Animation des Rollen Systems**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einer oder mehreren der folgenden Objekt Zustands Konstanten: Zustands System mit nicht Verfüg [**\_ \_ barem**](object-state-constants.md) Zustands System mit \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> Weitere Informationen finden Sie unter [Objektstatus Konstanten](object-state-constants.md).<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





