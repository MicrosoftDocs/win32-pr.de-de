---
title: Registerkartensteuerelement (MSAA UI-Elementreferenz)
description: Ein Registerkartensteuerelement definiert mehrere Seiten für den gleichen Bereich eines Fensters oder Dialogfelds.
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fe3216194da590b0c0802343afc41b1f7765c13d194e533163f9af2c22b287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505660"
---
# <a name="tab-control-msaa-ui-element-reference"></a>Registerkartensteuerelement (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Registerkartensteuerelementobjekte** für zwecke der MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Registerkartensteuerelement-Objekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Ein Registerkartensteuerelement definiert mehrere Seiten für den gleichen Bereich eines Fensters oder Dialogfelds. Jede Seite besteht aus einer Reihe von Informationen oder einer Gruppe von Steuerelementen, die eine Anwendung anzeigt, wenn der Benutzer die entsprechende Registerkarte auswählt. Das Windows Betriebssystem verwendet Registerkartensteuerelemente, um die Taskleistenschaltflächen mit Ausnahme der Schaltfläche **Start** anzuzeigen.

Der Fensterklassenname für ein Registerkartensteuerelement ist WC \_ TABCONTROL, das in Commctrl.h als "SysTabControl" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Registerkartensteuerelement unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Methode                                                                    | Kommentare                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Die [**accDoDefaultAction-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) klickt auf die Registerkarte "Seite". |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Registerkartensteuerelement unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Die **DefaultAction-Eigenschaft** ist "Switch".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** ist die Zugriffstaste des Registerkartensteuerelements, bei der es sich um ein unterstrichenes Zeichen im Fenstertext des Steuerelements handelt. Diese Zeichenfolge enthält das Anfügen des Zugriffsschlüsselzeichens an die Zeichenfolge "ALT+".                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** wird aus dem Fenstertext (oder der Beschriftung) des Steuerelements abgerufen, der im Registerkartensteuerelement angezeigt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ PAGETABLIST**](object-roles.md) ), das das Steuerelement umschließt und den gleichen Fensterklassennamen wie das Steuerelement hat.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ PAGETAB.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus einem oder mehreren der folgenden [Werte:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ SELECTABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ SELECTED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ PRESSED**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Hinweise

Registerkartensteuerelemente geben fälschlicherweise S \_ OK von der [**accSelect-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) zurück, wenn sie mit dem [**SELFLAG \_ TAKEFOCUS-Flag**](selflag.md) aufgerufen werden. Registerkartensteuerelemente können den Tastaturfokus nicht übernehmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





