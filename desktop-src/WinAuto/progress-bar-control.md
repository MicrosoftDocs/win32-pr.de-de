---
title: Statusanzeige-Steuerelement (MSAA UI-Elementreferenz)
description: Statusanzeige-Steuerelemente geben den Fortschritt eines längeren Vorgangs an, z. B. das Herunterladen einer Datei aus dem Internet. In der Regel wird der Fortschritt als Prozentsatz von null (0) bis 100 (100) ausgedrückt.
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a96b692de7b4c3992bab82eaa2461ce2826e5117498c24be7d8e40913d8a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052558"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a>Statusanzeige-Steuerelement (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Progress Bar Control-Objekte** für die MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Statusleisten-Steuerelementobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Statusanzeige-Steuerelemente geben den Fortschritt eines längeren Vorgangs an, z. B. das Herunterladen einer Datei aus dem Internet. In der Regel wird der Fortschritt als Prozentsatz von null (0) bis 100 (100) ausgedrückt.

Der Fensterklassenname für ein Statusanzeige-Steuerelement lautet PROGRESS \_ CLASS, der in Commctrl.h als "msctls progress" definiert \_ ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Statusanzeige-Steuerelemente unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Statusanzeige-Steuerelemente unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** ist die Zugriffstaste der Statusleiste, bei der es sich um ein unterstrichenes Zeichen im Text der Bezeichnung für die Statusanzeige handelt. Die zurückgegebene Zeichenfolge enthält das Anfügen des Zugriffsschlüsselzeichens an die Zeichenfolge "ALT+".                                                                                                                                                                                                                                 |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** ist der Text aus einem statischen Textsteuerelement, das die Statusanzeige bezeichnet.                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das Steuerelement verfügt.                                                                                                                                                                                                                                                              |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ PROGRESSBAR.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus einem oder mehreren der folgenden [Werte:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | Die **Value-Eigenschaft** ist eine Zeichenfolge von "0%" bis "100%", die den Fortschritt beschreibt.                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





