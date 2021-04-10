---
title: Bild Lauf Leiste (MSAA UI Element Reference)
description: Mithilfe von Bild Lauf leisten können Benutzer die Richtung und die Entfernung auswählen, um einen Bildlauf durch die Informationen in einem verwandten Fenster oder Listenfeld durchführen Der Fenster Klassenname für eine Schiebe Leiste lautet \ 0034; ScrollBar \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039551"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Bild Lauf Leiste (MSAA UI Element Reference)

> [!Note]  
> In diesem Thema werden **ScrollBar** -Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Das Erstellen von **ScrollBar** -Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Mithilfe von Bild Lauf leisten können Benutzer die Richtung und die Entfernung auswählen, um einen Bildlauf durch die Informationen in einem verwandten Fenster oder Listenfeld durchführen Der Fenster Klassenname für eine Schiebe Leiste ist "ScrollBar".

Der Inhalt der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften hängt davon ab, ob die Bild Lauf Leiste vertikal oder horizontal ist und ob die folgenden Teile der Bild Lauf Leiste vom Client abgefragt werden:

-   Die Scrollleiste selbst
-   Die obere oder nach-rechts-Taste
-   Schaltfläche "unten" oder "nach links"
-   Das Bild Lauf Feld (Thumb)
-   Der Bild-auf-oder Seiten rechten Bereich
-   Die Bild-ab-oder linke Seite

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Eine Schiebe Leiste unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)– das Bild Lauf leisten Objekt selbst und der Bild Lauf Zieh Punkt unterstützen die Methode " **accDoDefaultAction** " nicht.

    Für die anderen Bild Lauf leisten Teile auf einer vertikalen Bild Lauf Leiste ruft " [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) " [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit der " [**WM \_ VScroll**](/windows/desktop/Controls/wm-vscroll) "-Meldung auf, wobei *wParam* auf die folgenden Werte festgelegt ist.

    

    | Schaltfläche/Region       | Erwarteter        |
    |---------------------|--------------|
    | Schaltfläche "Oberer Pfeil    | SB \_ -Auflistung   |
    | Schaltfläche zum unteren Pfeil | SB- \_ LineDown |
    | Bild-auf-Seite      | SB- \_ PageUp   |
    | Bild-ab-Region    | SB- \_ PageDown |

    

     

    Für die anderen Bild Lauf leisten Teile auf einer horizontalen Schiebe Leiste ruft [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit der [**WM- \_ HScroll**](/windows/desktop/Controls/wm-hscroll) -Nachricht auf, wobei *wParam* auf die folgenden Werte festgelegt ist.

    

    | Schaltfläche/Region      | Wert         |
    |--------------------|---------------|
    | Schaltfläche nach links  | SB- \_ LineLeft  |
    | Schaltfläche mit Pfeil nach rechts | SB- \_ LineRight |
    | Seiten Linker Bereich   | SB- \_ PageLeft  |
    | Seite Rechter Bereich  | SB- \_ PageRight |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Eine Schiebe Leiste unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)– die **childCount** -Eigenschaft für das ScrollBar-Objekt ist 5. Für die anderen Bild Lauf leisten Teile ist die **childCount** -Eigenschaft gleich 0 (null).
-   [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)– das ScrollBar-Objekt selbst und der Bild Lauf Zieh Punkt unterstützen die **DEFAULTACTION** -Eigenschaft nicht. Die **DEFAULTACTION** -Eigenschaft für die Pfeil Schaltflächen und die schattierten Bereiche auf beiden Seiten des Bild Lauf Zieh Punkts sind "drücken".
-   [**get \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)– die **Description** -Eigenschaft hängt von dem Teil der Scrollleiste ab, der abgefragt wird.

    Die Teile einer vertikalen Schiebe Leiste enthalten die folgenden Beschreibungen.

    

    | Teil                | BESCHREIBUNG                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Scrollleiste selbst   | "Wird verwendet, um den vertikalen Anzeigebereich zu ändern."                                          |
    | Schaltfläche "Oberer Pfeil    | "Verschiebt die vertikale Position um eine Zeile nach oben"                                           |
    | Schaltfläche zum unteren Pfeil | "Verschiebt die vertikale Position um eine Zeile nach unten"                                         |
    | Bild Lauf Thumb        | "Gibt die aktuelle vertikale Position an und kann gezogen werden, um Sie direkt zu ändern." |
    | Bild-auf-Seite      | "Verschiebt die vertikale Position um einige Zeilen nach oben"                                  |
    | Bild-ab-Region    | "Gibt die aktuelle vertikale Position an und kann gezogen werden, um Sie direkt zu ändern." |

    

     

    Die Teile einer horizontalen Schiebe Leiste haben folgende Beschreibungen.

    

    | Teil               | BESCHREIBUNG                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Scrollleiste selbst  | "Wird verwendet, um den horizontalen Anzeigebereich zu ändern.                                          |
    | Schaltfläche nach links  | "Verschiebt die horizontale Position um eine Spalte nach links"                                       |
    | Schaltfläche mit Pfeil nach rechts | ' Verschiebt die horizontale Position um eine Spalte nach rechts                                      |
    | Bild Lauf Thumb       | "Gibt die aktuelle horizontale Position an und kann gezogen werden, um Sie direkt zu ändern." |
    | Seiten Linker Bereich   | "Verschiebt die horizontale Position um eine Reihe von Spalten nach links"                              |
    | Seite Rechter Bereich  | "Gibt die aktuelle vertikale Position an und kann gezogen werden, um Sie direkt zu ändern."   |

    

     

-   [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– die **Name** -Eigenschaft hängt von dem Teil der Scrollleiste ab, der abgefragt wird.

    Die Teile einer vertikalen Scrollleiste haben die folgenden Namen.

    | Teil                | Name        |
    |---------------------|-------------|
    | ScrollBar-Fenster   | Rechtes  |
    | Schaltfläche "Oberer Pfeil    | "Zeile nach oben"   |
    | Schaltfläche zum unteren Pfeil | "Zeile nach unten" |
    | Bild Lauf Thumb        | Gebracht  |
    | Bild-auf-Seite      | "Seite nach oben"   |
    | Bild-ab-Region    | "Bild-ab" |

    

     

    Die Teile einer horizontalen Scrollleiste haben die folgenden Namen.

    

    | Teil               | Name           |
    |--------------------|----------------|
    | ScrollBar-Fenster  | Ales   |
    | Schaltfläche nach links  | "Spalte links"  |
    | Schaltfläche mit Pfeil nach rechts | "Column right" |
    | Bild Lauf Thumb       | Gebracht     |
    | Seite Rechter Bereich  | "Page Right"   |
    | Seiten Linker Bereich   | "Seite Links"    |

    

     

-   [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)– die **Parent** -Eigenschaft der Pfeil Schaltflächen, der Bild Lauf Zieh Punkt und der schattierte Bereich auf beiden Seiten des Zieh Punkts ist das Fenster der Schiebe Leiste. Die **Parent** -Eigenschaft des ScrollBar-Fensters ist ein Fenster (Rollen \_ System \_ Fenster), das das Steuerelement umgibt und die **Name** -Eigenschaft und den Fenster Klassennamen aufweist.
-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– die **Role** -Eigenschaft hängt von dem Teil der Scrollleiste ab, der abgefragt wird. Die Teile einer Scrollleiste haben die folgenden Rollen. 

    | Teil                                                  | Role                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | Scrollleiste selbst                                     | [**Rollen \_ System- \_ Scrollleiste**](object-roles.md)   |
    | Schaltflächen oben, nach unten, Links und nach rechts              | [**\_ \_ Schaltfläche "Rollen System"**](object-roles.md) |
    | Bild Lauf Thumb                                          | [**Rollen \_ System \_ Indikator**](object-roles.md)   |
    | Bild-auf, Bild-ab, Seite Links und Seiten Rechte | [**\_ \_ Schaltfläche "Rollen System"**](object-roles.md) |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)– die **State** -Eigenschaft jeder ScrollBar-Komponente enthält eine Kombination der folgenden [Werte](object-state-constants.md).

    | State                                                                                 | Wert                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**Zustands \_ System \_ unsichtbar**](object-state-constants.md)     | In der Bild Lauf Leiste selbst gibt dies an, dass die angegebene vertikale oder horizontale Schiebe Leiste nicht vorhanden ist. Dies bedeutet, dass für die Bild-auf-oder-nach-unten-Bereiche der Ziehpunkt so positioniert ist, dass der Bereich nicht vorhanden ist. |
    | [**Zustands \_ System- \_ Offscreen**](object-state-constants.md)     | In der Bild Lauf Leiste selbst gibt dies an, dass das Fenster so groß ist, dass die angegebene vertikale oder horizontale Schiebe Leiste momentan nicht angezeigt wird.                                                                         |
    | [**Zustands \_ System wurde \_ gedrückt**](object-state-constants.md)         | Die Pfeil Schaltfläche oder der Seitenbereich wird gedrückt.                                                                                                                                                                                 |
    | [**Zustands \_ System nicht \_ verfügbar**](object-state-constants.md) | Die Komponente ist deaktiviert.                                                                                                                                                                                                  |

    

     

-   [**\_ accValue erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)– die Eigenschaft **Wert** für das Fenster Scrollleiste gibt die Position der Scrollleiste an und ist eine Zeichenfolge, die eine ganze Zahl zwischen 0 und 100 enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 