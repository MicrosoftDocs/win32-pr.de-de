---
title: Kombinations Feld (MSAA-Benutzeroberflächen-Element Referenz)
description: Ein Kombinationsfeld ist ein Listenfeld, das mit einem statischen Steuerelement oder einem Bearbeitungssteuerelement kombiniert ist und das momentan ausgewählte Element im Listenfeldbereich des Kombinationsfelds anzeigt.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce42bb3b0316b0fb2668fed23564b8f904fc793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711099"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Kombinations Feld (MSAA-Benutzeroberflächen-Element Referenz)

> [!Note]  
> In diesem Thema werden Kombinations **Feld** -Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Die Vorgehensweise zum Erstellen von Kombinations **Feld** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein Kombinationsfeld ist ein Listenfeld, das mit einem statischen Steuerelement oder einem Bearbeitungssteuerelement kombiniert ist und das momentan ausgewählte Element im Listenfeldbereich des Kombinationsfelds anzeigt. Der Listenfeld Bereich des Steuer Elements wird jederzeit oder nur Dropdown angezeigt, wenn der Benutzer den Dropdown Pfeil (der eine Schaltfläche ist) neben dem Steuerelement auswählt. Wenn das Auswahlfeld ein Bearbeitungs Steuerelement ist, kann der Benutzerinformationen eingeben, die nicht in der Liste enthalten sind. Andernfalls kann der Benutzer nur Elemente in der Liste auswählen.

Der Fenster Klassenname für ein Kombinations Feld ist "ComboBox".

Der Inhalt der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften hängt davon ab, welcher der folgenden Teile des Kombinations Felds vom Client abgefragt wird:

-   Kombinations Feld Fenster
-   Das Bearbeitungs Steuerelement oder das statische Text Steuerelement
-   Der Dropdown Pfeil (bei dem es sich um eine Schaltfläche "Push" handelt)
-   Das Listenfeld
-   Die Listenelemente im Listenfeld

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Kombinations Felder unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Kombinations Felder unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:

-   [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)– in der folgenden Tabelle wird der Wert für die untergeordnete Anzahl für verschiedene Teile des Kombinations Felds angezeigt. 

    | Kombinations Feld Teil   | ChildCount               |
    |------------------|--------------------------|
    | Kombinations Feld Fenster | 3                        |
    | Bearbeitungssteuerelement     | 0                        |
    | Dropdown Pfeil  | 0                        |
    | Listenfeld         | Die Anzahl der Listenelemente. |
    | Listenelement        | 0                        |

    

     

-   [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)– die folgende Tabelle zeigt die **DEFAULTACTION** -Eigenschaft für verschiedene Teile eines Kombinations Felds. 

    | Kombinations Feld Teil   | DEFAULTACTION                                                  |
    |------------------|----------------------------------------------------------------|
    | Kombinations Feld Fenster | Keine                                                           |
    | Bearbeitungssteuerelement     | Keine                                                           |
    | Dropdown Pfeil  | "Open" oder "Close" (abhängig vom Status der Dropdown Liste) |
    | Listenfeld         | Keine                                                           |
    | Listenelement        | "Doppelklicken"                                                 |

    

     

-   [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)– die folgende Tabelle zeigt die **KeyboardShortcut** -Eigenschaft für verschiedene Teile eines Kombinations Felds. 

    | Kombinations Feld Teil   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Kombinations Feld Fenster | Zugriffsschlüssel der zugeordneten Bezeichnung |
    | Bearbeitungssteuerelement     | Keine                           |
    | Dropdown Pfeil  | "Alt + nach-unten"               |
    | Listenfeld         | Keine                           |
    | Listenelement        | Keine                           |

    

     

    Die Zugriffstaste für ein Kombinations Feld ist das unterstrichene Zeichen im Text von einem zugeordneten statischen Text Steuerelement, das das Kombinations Feld bezeichnet. Wenn beispielsweise ein Standard Dialogfeld geöffnet wird, das Dateien öffnet, z. b. in Microsoft WordPad, weist das Kombinations Feld mit der Bezeichnung "Dateityp:" die **KeyboardShortcut** "alt + t" auf.

-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– in der folgenden Tabelle wird die **Name** -Eigenschaft für verschiedene Teile eines Kombinations Felds angezeigt. 

    | Kombinations Feld Teil   | Name                                                           |
    |------------------|----------------------------------------------------------------|
    | Kombinations Feld Fenster | Statisches Text Steuerelement, das als Bezeichnung verwendet wird.                            |
    | Bearbeitungssteuerelement     | Statisches Text Steuerelement, das als Bezeichnung verwendet wird.                            |
    | Dropdown Pfeil  | "Open" oder "Close" (abhängig vom Status der Dropdown Liste) |
    | Listenfeld         | Zugehörige Bezeichnung                                               |
    | Listenelement        | Text des Listen Elements                                          |

    

     

    Die **Name** -Eigenschaft eines Kombinations Felds, das untergeordnete Bearbeitungs Steuerelement und das untergeordnete Listenfeld sind der Text aus einem zugeordneten statischen Text Steuerelement, das das Kombinations Feld bezeichnet. Beispielsweise werden in einem geöffneten Standard Dialogfeld Dateien, wie z. b. in WordPad, die **namens** Eigenschaften für die beiden Kombinations Felder "suchen in:" und "files of Type:" angezeigt.

-   [**get- \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)– die folgende Tabelle zeigt den übergeordneten Wert für verschiedene Teile eines Kombinations Felds. 

    | Kombinations Feld Teil                        | Parent                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Kombinations Feld Fenster                      | Ein Fenster mit der **Role** -Eigenschaft des [**Rollen \_ System \_ Fensters**](object-roles.md) , das das Kombinations Feld umgibt und die **Name** -Eigenschaft und den Fenster Klassennamen wie das Kombinations Feld aufweist. |
    | Steuerelement bearbeiten (oder statisches Text Steuerelement) | Das Kombinations Feld Fenster.                                                                                                                                                                                          |
    | Dropdown Pfeil                       | Das Kombinations Feld Fenster.                                                                                                                                                                                          |
    | Übergeordnetes Listenfeld Fenster                | Das Kombinations Feld Fenster. In diesem Fenster wird das Listenfeld umgeben.                                                                                                                                                      |
    | Listenfeld                              | Das übergeordnete Listenfeld Fenster.                                                                                                                                                                                    |
    | Listenelement                             | Das Listenfeld.                                                                                                                                                                                                  |

    

     

-   [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– in der folgenden Tabelle wird die **Role** -Eigenschaft für verschiedene Teile eines Kombinations Felds angezeigt. 

    | Kombinations Feld Teil                        | [Rolle](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | Kombinations Feld Fenster                      | [**Kombinations \_ Feld "Rollen System" \_**](object-roles.md)                                                                    |
    | Steuerelement bearbeiten (oder statisches Text Steuerelement) | [**Rolle \_ System \_ Text**](object-roles.md) oder [ **Rollen \_ System- \_ StaticText**](object-roles.md) |
    | Dropdown Pfeil                       | [**\_ \_ Schaltfläche "Rollen System"**](object-roles.md)                                                                |
    | Listenfeld                              | [**Liste der Rollen \_ Systeme \_**](object-roles.md)                                                                            |
    | Listenelement                             | [**Rollen \_ System ( \_ ListItem)**](object-roles.md)                                                                    |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)– die folgende Tabelle zeigt die **Zustands** Eigenschaft für verschiedene Teile eines Kombinations Felds. 

    | Kombinations Feld Teil   | [Mögliche Zustände](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Kombinations Feld Fenster | [**Status \_ System \_ unsichtbares**](object-state-constants.md) Zustands System mit System eigenem Zustands System, das für das Zustands System mit System eigenem Zustands System \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ fokussiert**](object-state-constants.md) ist \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) |
    | Bearbeitungssteuerelement     | [**Status \_ System \_ unsichtbares**](object-state-constants.md) Zustands System mit Fokus Zustands System mit \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)                                                                                                                                                                         |
    | Dropdown Pfeil  | 0 bedeutet, dass die Schaltfläche sichtbar und nicht gedrückt ist. oder [**Zustands System mit \_ \_ gedrücktem**](object-state-constants.md) Zustands System \| [**\_ \_ unsichtbar**](object-state-constants.md) \| \_ \_                                                                                                                                                                                                                                                                                                                                                    |
    | Listenfeld         | [**Status \_ System \_ unsichtbares**](object-state-constants.md) Zustands System mit \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ Fokus**](object-state-constants.md) Zustands \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) System für System eigenes Zustands System                                                                                      |
    | Listenelement        | [**Status \_ System \_ unsichtbares**](object-state-constants.md) Zustands System für System eigenes Zustands System mit \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ aktiviertem**](object-state-constants.md) Zustands System \| ausgewählt [**\_ \_**](object-state-constants.md) Zustands System \| [**\_ \_ ausgewählt**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)                                                                                        |

    

     

-   [**\_ accValue erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)– in der folgenden Tabelle wird die **value** -Eigenschaft für verschiedene Teile eines Kombinations Felds angezeigt. 

    | Kombinations Feld Teil   | Wert                                |
    |------------------|--------------------------------------|
    | Kombinations Feld Fenster | Text des aktuell ausgewählten Listen Elements |
    | Bearbeitungssteuerelement     | Text des aktuell ausgewählten Listen Elements |
    | Dropdown Pfeil  | Keine                                 |
    | Listenfeld         | Keine                                 |
    | Listenelement        | Keine                                 |

    

     

## <a name="notes"></a>Notizen

-   Wenn " [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) " mit dem [**navDir \_ Next**](navigation-constants.md) -Flag im Listenfeld Teil eines Kombinations Felds aufgerufen wird, wechselt es fälschlicherweise zum Task leisten Fenster, wenn " **VT \_ empty**" zurückgegeben werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




