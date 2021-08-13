---
title: Schieberegler-Steuerelement (MSAA UI-Elementreferenz)
description: Mit einem Schieberegler-Steuerelement, das auch als Trackbar-Steuerelement bezeichnet wird, kann ein Benutzer aus einem Bereich von Werten auswählen, indem er einen Schieberegler bewegt. Unter dem Betriebssystem Windows werden Schieberegler-Steuerelemente zum Einstellen der Lautstärke verwendet.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d92799a8a644d5e5e00c695d628cb827ba60f73cc3a0d7b7f5dc505a6c2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564428"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Schieberegler-Steuerelement (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Slider Control-Objekte** für zwecke der MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Schieberegler-Steuerelementobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Mit einem Schieberegler-Steuerelement, das auch als Trackbar-Steuerelement bezeichnet wird, kann ein Benutzer aus einem Bereich von Werten auswählen, indem er einen Schieberegler bewegt. Unter dem Betriebssystem Windows werden Schieberegler-Steuerelemente zum Einstellen der Lautstärke verwendet.

Der Name der Fensterklasse für ein Schieberegler-Steuerelement ist TRACKBAR \_ CLASS, die in Commctrl.h als "msctls \_ trackbar" definiert ist.

Der Inhalt der [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) hängt davon ab, ob der Schieberegler vertikal oder horizontal ist und von welchen der folgenden Teile des Schieberegler-Steuerelements vom Client abgefragt wird:

-   Schiebereglerfenster
-   Schieberegler
-   Schattierten Bereich über (oder an)
-   Schattierten Bereich unter (oder rechts von) dem Schiebereglerfinger

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Schieberegler-Steuerelement unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Schieberegler-Steuerelement unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)– Die **KeyboardShortcut-Eigenschaft** ist die Zugriffstaste des Schiebereglerfensters, die ein unterstrichenes Zeichen im Text der Bezeichnung für den Schieberegler ist. Die zurückgegebene Zeichenfolge enthält das Anfügen des Zugriffsschlüsselzeichens an die Zeichenfolge "ALT+".
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): Die **Name-Eigenschaft** hängt von dem Teil des abgefragten Schiebereglers ab.

    Die Teile eines vertikalen Schiebereglers haben die folgenden Namen:

    

    | Schiebereglerteil                    | Name                                |
    |--------------------------------|-------------------------------------|
    | Schiebereglerfenster                  | Statisches Textsteuerelement, das als Bezeichnung verwendet wird |
    | Schieberegler                   | "Position"                          |
    | Schattierte Fläche über dem Schiebereglerfinger | "Vorherige Seite"                           |
    | Schattierte Fläche unterhalb des Schiebereglers | "Nächste Seite"                         |

    

     

    Die Teile eines horizontalen Schiebereglers haben die folgenden Namen:

    

    | Schiebereglerteil                              | Name                                |
    |------------------------------------------|-------------------------------------|
    | Schiebereglerfenster                            | Statisches Textsteuerelement, das als Bezeichnung verwendet wird |
    | Schieberegler                             | "Position"                          |
    | Schattierten Bereich links vom Schieberegler  | "Seite links"                         |
    | Schattierten Bereich rechts neben dem Schieberegler | "Seite rechts"                        |

    

     

-   [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)– Die **parent-Eigenschaft** der Pfeilschaltflächen, des Bildlauffingers, und der schattierte Bereich auf beiden Seiten des Ziehfelds ist das Schiebereglerfenster. Die **Parent-Eigenschaft** des Schiebereglerfensters ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen verfügt.
-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): Die **Role-Eigenschaft** hängt von dem Teil des abgefragten Schiebereglers ab. 

    | Schiebereglerteil                                     | [Rolle](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Schiebereglerfenster                                   | [**\_ \_ ROLLENSYSTEMSCHIEBEREGLER**](object-roles.md)         |
    | Schieberegler                                    | [**ROLE \_ SYSTEM \_ INDICATOR**](object-roles.md)   |
    | Schattierte Bereiche auf beiden Seiten des Schiebereglers | [**\_ \_ ROLLENSYSTEM-PUSHBUTTON**](object-roles.md) |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate):[Die Werte](object-state-constants.md) für die **State-Eigenschaft** hängen von dem Teil des abgefragten Schiebereglers ab. 

    | Schiebereglerteil                                     | Mögliche Statuswerte                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Schiebereglerfenster                                   | [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md) |
    | Schieberegler                                    | Null (0), was bedeutet, dass das Objekt sichtbar ist, oder [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md)                                                                                                                       |
    | Schattierte Bereiche auf beiden Seiten des Schiebereglers | Null (0), was bedeutet, dass das Objekt sichtbar ist, oder [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md)                                                                                                                       |

    

     

-   [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)– Die **Value-Eigenschaft** für das Schiebereglerfenster gibt die Position des Ziehwerts an und ist eine Zeichenfolge, die eine ganze Zahl von "0" bis "100" enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Scrollleiste**](scroll-bar.md)
</dt> </dl>

 

 




