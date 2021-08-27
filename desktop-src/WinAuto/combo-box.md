---
title: Kombinationsfeld (REFERENZ ZUM MSAA-UI-Element)
description: Ein Kombinationsfeld ist ein Listenfeld, das mit einem statischen Steuerelement oder einem Bearbeitungssteuerelement kombiniert ist und das momentan ausgewählte Element im Listenfeldbereich des Kombinationsfelds anzeigt.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3a8d26fa5b8cb264c06e7aa64c672e0a80e8ada7e90a152b3b941ea207cade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071840"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Kombinationsfeld (REFERENZ ZUM MSAA-UI-Element)

> [!Note]  
> In diesem Thema werden **Combo Box-Objekte** für die MSAA-Benutzeroberflächenelementreferenz beschrieben. Das Erstellen von **Combo Box-Objekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenzdokumentation für das benutzeroberflächenframework, das Sie verwenden.

 

Ein Kombinationsfeld ist ein Listenfeld, das mit einem statischen Steuerelement oder einem Bearbeitungssteuerelement kombiniert ist und das momentan ausgewählte Element im Listenfeldbereich des Kombinationsfelds anzeigt. Der Listenfeldteil des Steuerelements wird jederzeit oder nur dann in der Dropdownliste angezeigt, wenn der Benutzer den Dropdownpfeil (bei dem es sich um eine Schaltfläche handelt) neben dem Steuerelement auswählt. Wenn das Auswahlfeld ein Bearbeitungssteuerfeld ist, kann der Benutzer Informationen eingeben, die nicht in der Liste enthalten sind. Andernfalls kann der Benutzer nur Elemente in der Liste auswählen.

Der Name der Fensterklasse für ein Kombinationsfeld ist "COMBOBOX".

Der Inhalt der [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) hängt davon ab, welcher der folgenden Teile des Kombinationsfelds vom Client abgefragt wird:

-   Das Kombinationsfeldfenster
-   Das Bearbeitungssteuerfeld oder das statische Textsteuerfeld
-   Der Dropdownpfeil (bei dem es sich um eine Schaltfläche handelt)
-   Das Listenfeld
-   Die Listenelemente im Listenfeld

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Kombinationsfelder unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Kombinationsfelder unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**get \_ accChildCount :**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)In der folgenden Tabelle wird der Wert der untergeordneten Anzahl für verschiedene Teile des Kombinationsfelds angezeigt. 

    | Kombinationsfeldteil   | ChildCount               |
    |------------------|--------------------------|
    | Kombinationsfeldfenster | 3                        |
    | Bearbeitungssteuerelement     | 0                        |
    | Dropdownpfeil  | 0                        |
    | Listenfeld         | Die Anzahl der Listenelemente |
    | Listenelement        | 0                        |

    

     

-   [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): Die folgende Tabelle zeigt die **DefaultAction-Eigenschaft** für verschiedene Teile eines Kombinationsfelds. 

    | Kombinationsfeldteil   | Defaultaction                                                  |
    |------------------|----------------------------------------------------------------|
    | Kombinationsfeldfenster | Keiner                                                           |
    | Bearbeitungssteuerelement     | Keiner                                                           |
    | Dropdownpfeil  | "Öffnen" oder "Schließen" je nach Status der Dropdownliste |
    | Listenfeld         | Keiner                                                           |
    | Listenelement        | "Doppelklicken"                                                 |

    

     

-   [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)– Die folgende Tabelle zeigt die **KeyboardShortcut-Eigenschaft** für verschiedene Teile eines Kombinationsfelds. 

    | Kombinationsfeldteil   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Kombinationsfeldfenster | Zugriffsschlüssel der zugeordneten Bezeichnung |
    | Bearbeitungssteuerelement     | Keiner                           |
    | Dropdownpfeil  | "ALT+NACH-UNTEN-TASTE"               |
    | Listenfeld         | Keiner                           |
    | Listenelement        | Keiner                           |

    

     

    Die Zugriffsschlüssel für ein Kombinationsfeld ist das unterstrichene Zeichen im Text eines zugeordneten statischen Textsteuerfelds, das das Kombinationsfeld bezeichnet. In einem Standarddialogfeld öffnen, in dem Dateien geöffnet werden, z. B. in Microsoft WordPad, hat das Kombinationsfeld mit der Bezeichnung "Dateien des Typs:" den **Tastaturbefehl** "Alt+t".

-   [**get \_ accName :**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)In der folgenden Tabelle wird die **Name-Eigenschaft** für verschiedene Teile eines Kombinationsfelds angezeigt. 

    | Kombinationsfeldteil   | Name                                                           |
    |------------------|----------------------------------------------------------------|
    | Kombinationsfeldfenster | Statisches Textsteuerfeld, das als Bezeichnung verwendet wird                            |
    | Bearbeitungssteuerelement     | Statisches Textsteuerfeld, das als Bezeichnung verwendet wird                            |
    | Dropdownpfeil  | "Öffnen" oder "Schließen" je nach Status der Dropdownliste |
    | Listenfeld         | Zugeordnete Bezeichnung                                               |
    | Listenelement        | Text des Listenelements                                          |

    

     

    Die **Name-Eigenschaft** eines Kombinationsfelds, das untergeordnete Bearbeitungssteuerfeld und das untergeordnete Listenfeld sind der Text eines zugeordneten statischen Textsteuerfelds, das das Kombinationsfeld bezeichnet. In einem Standarddialogfeld öffnen, das Dateien öffnet, z.  B. in WordPad, sind die Name-Eigenschaften für die beiden Kombinationsfelder "Look in:" und "Files of type:".

-   [**get \_ accParent :**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)In der folgenden Tabelle wird der übergeordnete Wert für verschiedene Teile eines Kombinationsfelds angezeigt. 

    | Kombinationsfeldteil                        | Parent                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Kombinationsfeldfenster                      | Ein Fenster mit der **Role-Eigenschaft** von [**ROLE SYSTEM \_ \_ WINDOW,**](object-roles.md) das das Kombinationsfeld umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das Kombinationsfeld verfügt. |
    | Steuerelement bearbeiten (oder statisches Textsteuerfeld) | Das Kombinationsfeldfenster.                                                                                                                                                                                          |
    | Dropdownpfeil                       | Das Kombinationsfeldfenster.                                                                                                                                                                                          |
    | Übergeordnetes Listenfeldfenster                | Das Kombinationsfeldfenster. Dieses Fenster umschließt das Listenfeld.                                                                                                                                                      |
    | Listenfeld                              | Das übergeordnete Listenfeldfenster.                                                                                                                                                                                    |
    | Listenelement                             | Das Listenfeld.                                                                                                                                                                                                  |

    

     

-   [**get \_ accRole :**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)Die folgende Tabelle zeigt die **Role-Eigenschaft** für verschiedene Teile eines Kombinationsfelds. 

    | Kombinationsfeldteil                        | [Rolle](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | Kombinationsfeldfenster                      | [**KOMBINATIONSFELD \_ \_ "ROLLENSYSTEM"**](object-roles.md)                                                                    |
    | Steuerelement bearbeiten (oder statisches Textsteuerfeld) | [**ROLE \_ \_SYSTEMTEXT**](object-roles.md) oder [ **ROLE SYSTEM \_ \_ STATICTEXT**](object-roles.md) |
    | Dropdownpfeil                       | [**\_ \_ ROLLENSYSTEM-PUSHBUTTON**](object-roles.md)                                                                |
    | Listenfeld                              | [**\_ \_ ROLLENSYSTEMLISTE**](object-roles.md)                                                                            |
    | Listenelement                             | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)                                                                    |

    

     

-   [**get \_ accState :**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)In der folgenden Tabelle wird die **State-Eigenschaft** für verschiedene Teile eines Kombinationsfelds angezeigt. 

    | Kombinationsfeldteil   | [Mögliche Zustände](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Kombinationsfeldfenster | [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM FOCUSED \| [**STATE \_ \_**](object-state-constants.md) \| [**\_ SYSTEM \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ EXPANDED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ COLLAPSED**](object-state-constants.md) |
    | Bearbeitungssteuerelement     | [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md)                                                                                                                                                                         |
    | Dropdownpfeil  | 0, was bedeutet, dass die Schaltfläche sichtbar ist und nicht gedrückt wird. oder [**STATE \_ SYSTEM \_ PRESSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| STATE SYSTEM \_ \_ NORMAL                                                                                                                                                                                                                                                                                                                                                    |
    | Listenfeld         | [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM FOCUSED STATE \| [**\_ \_**](object-state-constants.md) \| [**SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FLOATING**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)                                                                                      |
    | Listenelement        | [**STATE \_ SYSTEM \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ SELECTABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ SELECTED**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)                                                                                        |

    

     

-   [**get \_ accValue :**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)In der folgenden Tabelle wird die **Value-Eigenschaft** für verschiedene Teile eines Kombinationsfelds angezeigt. 

    | Kombinationsfeldteil   | Wert                                |
    |------------------|--------------------------------------|
    | Kombinationsfeldfenster | Text des aktuell ausgewählten Listenelements |
    | Bearbeitungssteuerelement     | Text des aktuell ausgewählten Listenelements |
    | Dropdownpfeil  | Keiner                                 |
    | Listenfeld         | Keiner                                 |
    | Listenelement        | Keiner                                 |

    

     

## <a name="notes"></a>Hinweise

-   Wenn [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) mit dem [**FLAG NAVDIR \_ NEXT**](navigation-constants.md) im Listenfeld eines Kombinationsfelds aufgerufen wird, navigiert es fälschlicherweise zum Taskleistenfenster, wenn VT EMPTY zurückgeben **\_ soll.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




