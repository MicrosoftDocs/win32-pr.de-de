---
title: Schieberegler-Steuer Element (MSAA UI-Element Referenz)
description: Ein Schieberegler-Steuerelement, das auch als TrackBar-Steuerelement bezeichnet wird, ermöglicht Benutzern die Auswahl aus einem Wertebereich durch Verschieben eines Schiebereglers. Unter dem Betriebssystem Windows werden Schieberegler-Steuerelemente zum Einstellen der Lautstärke verwendet.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037534"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Schieberegler-Steuer Element (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden **Schieberegler-Steuer** Element Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Hier wird beschrieben, wie Sie **Schieberegler-Steuer** Element Objekte in verschiedenen Benutzeroberflächen-Frameworks erstellen. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein Schieberegler-Steuerelement, das auch als TrackBar-Steuerelement bezeichnet wird, ermöglicht Benutzern die Auswahl aus einem Wertebereich durch Verschieben eines Schiebereglers. Unter dem Betriebssystem Windows werden Schieberegler-Steuerelemente zum Einstellen der Lautstärke verwendet.

Der Fenster Klassenname für ein Schieberegler-Steuerelement ist TrackBar \_ Class, das in der Datei "commctrl. h" als "msctls \_ TrackBar" definiert ist.

Der Inhalt der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften hängt davon ab, ob der Schieberegler vertikal oder horizontal ist und auf welchem der folgenden Teile des Schieberegler-Steuer Elements vom Client abgefragt wird:

-   Schieberegler-Fenster
-   Ziehpunkt
-   Schattierter Bereich oberhalb (oder bis
-   Schattierter Bereich unterhalb des Schieberegler-Zieh Punkts (oder rechts von)

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Ein Schieberegler-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Schieberegler-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:

-   [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)– die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste des Schieberegler-Fensters, bei der es sich um ein unterstrichenes Zeichen im Text der Bezeichnung für den Schieberegler handelt. Die zurückgegebene Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird.
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– die **Name** -Eigenschaft hängt von dem Teil des Schiebereglers ab, der abgefragt wird.

    Die Teile eines vertikalen Schiebereglers haben die folgenden Namen:

    

    | Schieberegler-Teil                    | Name                                |
    |--------------------------------|-------------------------------------|
    | Schieberegler-Fenster                  | Statisches Text Steuerelement, das als Bezeichnung verwendet wird. |
    | Ziehpunkt                   | Gebracht                          |
    | Schattierter Bereich oberhalb des Schiebereglers | "Seite nach oben"                           |
    | Schattierter Bereich unterhalb des Schiebereglers | "Bild-ab"                         |

    

     

    Die Teile eines horizontalen Schiebereglers haben die folgenden Namen:

    

    | Schieberegler-Teil                              | Name                                |
    |------------------------------------------|-------------------------------------|
    | Schieberegler-Fenster                            | Statisches Text Steuerelement, das als Bezeichnung verwendet wird. |
    | Ziehpunkt                             | Gebracht                          |
    | Schattierter Bereich auf der linken Seite des Schiebereglers  | "Seite Links"                         |
    | Schattierter Bereich rechts vom Schieberegler-Ziehpunkt | "Page Right"                        |

    

     

-   [**get- \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)– die **Parent** -Eigenschaft der Pfeil Schaltflächen, der Bild Lauf Thumb und der schattierte Bereich auf beiden Seiten des Zieh Punkts ist das Schieberegler-Fenster. Die **Parent** -Eigenschaft des Schieberegler-Fensters ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die **Name** -Eigenschaft und den Fenster Klassennamen aufweist.
-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– die **Role** -Eigenschaft hängt von dem Teil des Schiebereglers ab, der abgefragt wird. 

    | Schieberegler-Teil                                     | [Rolle](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Schieberegler-Fenster                                   | [**\_ \_ Schieberegler für Rollen System**](object-roles.md)         |
    | Ziehpunkt                                    | [**Rollen \_ System \_ Indikator**](object-roles.md)   |
    | Schattierte Bereiche auf beiden Seiten des Schiebereglers | [**\_ \_ Schaltfläche "Rollen System"**](object-roles.md) |

    

     

-   die [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)–-[Werte](object-state-constants.md) für die **State** -Eigenschaft sind abhängig von dem Teil des Schiebereglers, der abgefragt wird. 

    | Schieberegler-Teil                                     | Mögliche Zustands Werte                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Schieberegler-Fenster                                   | [**Status \_ System \_ unsichtbares**](object-state-constants.md) Zustands System mit Fokus Zustands System mit \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) |
    | Ziehpunkt                                    | NULL (0), d. h. das Objekt ist sichtbar [**, \_ \_ oder das**](object-state-constants.md) nicht verfügbare Zustands System ist nicht \| [**\_ \_ verfügbar**](object-state-constants.md) . \| [**\_ \_**](object-state-constants.md)                                                                                                                       |
    | Schattierte Bereiche auf beiden Seiten des Schiebereglers | NULL (0), d. h. das Objekt ist sichtbar [**, \_ \_ oder das**](object-state-constants.md) nicht verfügbare Zustands System ist nicht \| [**\_ \_ verfügbar**](object-state-constants.md) . \| [**\_ \_**](object-state-constants.md)                                                                                                                       |

    

     

-   [**get- \_ Wert**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)– die **value** -Eigenschaft für das Schieberegler-Fenster gibt die Position des Zieh Punkts an und ist eine Zeichenfolge, die eine ganze Zahl zwischen "0" und "100" enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Scrollleiste**](scroll-bar.md)
</dt> </dl>

 

 




