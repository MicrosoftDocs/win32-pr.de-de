---
title: Scrollleiste (MSAA UI-Elementreferenz)
description: Mithilfe von Bildlaufleisten können Benutzer die Richtung und den Abstand auswählen, in der bzw. dem informationen in einem verknüpften Fenster oder Listenfeld angezeigt werden sollen. Der Name der Fensterklasse für eine Bildlaufleiste lautet \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6acb609ee56d6e766a2f94cf75406211741ba0a711699f4e8c912790dc71cffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734330"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Scrollleiste (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Scrollleistenobjekte** für die MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Scrollleistenobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Mithilfe von Bildlaufleisten können Benutzer die Richtung und den Abstand auswählen, in der bzw. dem informationen in einem verknüpften Fenster oder Listenfeld angezeigt werden sollen. Der Name der Fensterklasse für eine Bildlaufleiste lautet "SCROLLBAR".

Der Inhalt der [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) hängt davon ab, ob die Scrollleiste vertikal oder horizontal ist und von welchem der folgenden Teile der Scrollleiste vom Client abgefragt wird:

-   Die Bildlaufleiste selbst
-   Schaltfläche "Pfeil nach oben" oder "Nach rechts"
-   Schaltfläche "Unten" oder "Pfeil nach links"
-   Das Bildlauffeld ( Thumb)
-   Die Region nach oben oder rechts der Seite
-   Die Nach-unten-Seite oder der linke Bereich der Seite

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Eine Bildlaufleiste unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction): Das Scrollleistenobjekt selbst und der Bildlauffinger unterstützen die **accDoDefaultAction-Methode** nicht.

    Für die anderen Teile der Bildlaufleiste auf einer vertikalen Schiebeleiste ruft [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) auf, wobei die [**\_ WM-VSCROLL-Nachricht**](/windows/desktop/Controls/wm-vscroll) mit *wParam* auf die folgenden Werte festgelegt ist.

    

    | Schaltfläche/Region       | Vaule        |
    |---------------------|--------------|
    | Schaltfläche "Pfeil oben"    | SB \_ LINEUP   |
    | Schaltfläche "Pfeil unten" | SB \_ LINEDOWN |
    | Vorherige Seite Region      | SB \_ PAGEUP   |
    | Nächste Seite Region    | SB \_ PAGEDOWN |

    

     

    Für die anderen Bildlaufleistenteile auf einer horizontalen Scrollleiste ruft [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) auf, wobei die [**WM \_ HSCROLL-Nachricht**](/windows/desktop/Controls/wm-hscroll) mit *wParam* auf die folgenden Werte festgelegt ist.

    

    | Schaltfläche/Region      | Wert         |
    |--------------------|---------------|
    | Schaltfläche "Pfeil nach links"  | SB \_ LINELEFT  |
    | Schaltfläche mit Pfeil nach rechts | SB \_ LINERIGHT |
    | Linker Bereich der Seite   | SB \_ PAGELEFT  |
    | Rechte Region der Seite  | SB \_ PAGERIGHT |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Eine Bildlaufleiste unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)– Die **ChildCount-Eigenschaft** für das Scrollleistenobjekt ist fünf. Für die anderen Bildlaufleistenteile ist die **ChildCount-Eigenschaft** 0 (null).
-   [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): Das Bildlaufleistenobjekt selbst und der Bildlauffinger unterstützen die **DefaultAction-Eigenschaft** nicht. Die **DefaultAction-Eigenschaft** für die Pfeilschaltflächen und die schattierten Bereiche auf beiden Seiten des Bildlauffingerabdrucks lautet "Press".
-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)– Die **Description-Eigenschaft** hängt von dem Teil der abgefragten Scrollleiste ab.

    Die Teile einer vertikalen Bildlaufleiste weisen die folgenden Beschreibungen auf.

    

    | Teil                | Beschreibung                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Scrollleiste selbst   | "Wird verwendet, um den vertikalen Anzeigebereich zu ändern"                                          |
    | Schaltfläche "Pfeil oben"    | "Verschiebt die vertikale Position um eine Zeile nach oben"                                           |
    | Schaltfläche "Pfeil unten" | "Verschiebt die vertikale Position um eine Zeile nach unten"                                         |
    | Bildlauffinger        | "Gibt die aktuelle vertikale Position an und kann gezogen werden, um sie direkt zu ändern." |
    | Vorherige Seite Region      | "Verschiebt die vertikale Position um einige Zeilen nach oben"                                  |
    | Nächste Seite Region    | "Gibt die aktuelle vertikale Position an und kann gezogen werden, um sie direkt zu ändern." |

    

     

    Die Teile einer horizontalen Bildlaufleiste weisen die folgenden Beschreibungen auf.

    

    | Teil               | Beschreibung                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Scrollleiste selbst  | "Wird verwendet, um den horizontalen Anzeigebereich zu ändern"                                          |
    | Schaltfläche "Pfeil nach links"  | "Verschiebt die horizontale Position nach links um eine Spalte"                                       |
    | Schaltfläche mit Pfeil nach rechts | "Verschiebt die horizontale Position um eine Spalte nach rechts".                                      |
    | Bildlauffinger       | "Gibt die aktuelle horizontale Position an und kann gezogen werden, um sie direkt zu ändern." |
    | Linker Bereich der Seite   | "Verschiebt die horizontale Position nach links um einige Spalten".                              |
    | Rechte Region der Seite  | "Gibt die aktuelle vertikale Position an und kann gezogen werden, um sie direkt zu ändern."   |

    

     

-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): Die **Name-Eigenschaft** hängt von dem Teil der abgefragten Scrollleiste ab.

    Die Teile einer vertikalen Bildlaufleiste haben die folgenden Namen.

    | Teil                | Name        |
    |---------------------|-------------|
    | Bildlaufleistenfenster   | "Vertikal"  |
    | Schaltfläche "Pfeil oben"    | "Line up"   |
    | Schaltfläche "Pfeil unten" | "Line down" (Nach unten) |
    | Bildlauffinger        | "Position"  |
    | Vorherige Seite Region      | "Vorherige Seite"   |
    | Nächste Seite Region    | "Nächste Seite" |

    

     

    Die Teile einer horizontalen Bildlaufleiste haben die folgenden Namen.

    

    | Teil               | Name           |
    |--------------------|----------------|
    | Bildlaufleistenfenster  | "Horizontal"   |
    | Schaltfläche "Pfeil nach links"  | "Spalte links"  |
    | Schaltfläche mit Pfeil nach rechts | "Spalte rechts" |
    | Bildlauffinger       | "Position"     |
    | Rechte Region der Seite  | "Seite rechts"   |
    | Linker Bereich der Seite   | "Seite links"    |

    

     

-   [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)– Die **parent-Eigenschaft** der Pfeilschaltflächen, der Bildlauffinger, und der schattierte Bereich auf beiden Seiten des Ziehfelds ist das Scrollleistenfenster. Die **Parent-Eigenschaft** des Scrollleistenfensters ist ein Fenster (ROLE \_ SYSTEM \_ WINDOW), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen verfügt.
-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): Die **Role-Eigenschaft** hängt von dem Teil der abgefragten Scrollleiste ab. Die Teile einer Bildlaufleiste weisen die folgenden Rollen auf. 

    | Teil                                                  | Rolle                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | Scrollleiste selbst                                     | [**\_SCROLLLEISTE DES ROLLENSYSTEMS \_**](object-roles.md)   |
    | Schaltflächen "Oben", "Nach unten", "Links" und "Nach rechts"              | [**\_ \_ ROLLENSYSTEM-PUSHBUTTON**](object-roles.md) |
    | Bildlauffinger                                          | [**ROLE \_ SYSTEM \_ INDICATOR**](object-roles.md)   |
    | Vorherige Seite, Nach unten, Seite links und Seiten rechts | [**\_ \_ ROLLENSYSTEM-PUSHBUTTON**](object-roles.md) |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): Die **State-Eigenschaft** jeder Scrollleistenkomponente enthält eine Kombination der folgenden [Werte.](object-state-constants.md)

    | State                                                                                 | Wert                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**STATUSSYSTEM \_ \_ UNSICHTBAR**](object-state-constants.md)     | Für die Bildlaufleiste selbst gibt dies an, dass die angegebene vertikale oder horizontale Scrollleiste nicht vorhanden ist. Für die Bereiche nach oben oder nach unten zeigt dies an, dass der Daumen so positioniert ist, dass der Bereich nicht vorhanden ist. |
    | [**OFFSCREEN \_ DES ZUSTANDSSYSTEMS \_**](object-state-constants.md)     | Für die Bildlaufleiste selbst gibt dies an, dass das Fenster so dimensioniert ist, dass die angegebene vertikale oder horizontale Bildlaufleiste derzeit nicht angezeigt wird.                                                                         |
    | [**ZUSTANDSSYSTEM \_ \_ GEDRÜCKT**](object-state-constants.md)         | Die Pfeilschaltfläche oder der Seitenbereich wird gedrückt.                                                                                                                                                                                 |
    | [**STATUSSYSTEM \_ \_ NICHT VERFÜGBAR**](object-state-constants.md) | Die Komponente ist deaktiviert.                                                                                                                                                                                                  |

    

     

-   [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): Die **Value-Eigenschaft** für das Scrollleistenfenster gibt die Position der Scrollleiste an und ist eine Zeichenfolge, die eine ganze Zahl von "0" bis "100" enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 