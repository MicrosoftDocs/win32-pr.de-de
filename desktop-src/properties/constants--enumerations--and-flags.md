---
description: In diesem Abschnitt werden die Konstanten, Enumerationen und Flags des Windows-Eigenschafts Systems beschrieben.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: Konstanten, Enumerationen und Flags (Windows-Eigenschaften System)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8681c773181b69b24b1fe2d01d380d730c33e220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216258"
---
# <a name="constants-enumerations-and-flags"></a>Konstanten, Enumerationen und Flags

In diesem Abschnitt werden die Konstanten, Enumerationen und Flags des Windows-Eigenschafts Systems beschrieben.



| Thema                                                                              | Inhalte                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getpropertystoreflags**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Gibt Flags an, die das Eigenschafts Speicher Objekt ändern, das von Methoden abgerufen wird, die einen Eigenschafts Speicher erstellen, z. b. [**IShellItem2:: getpropertystore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) oder [**ipropertystorefactory:: getpropertystore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**Pdopstatus**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Stellt Vorgangs Status-Flags bereit.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**PKA- \_ Flags**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Beschreibt das Array Verhalten von Eigenschaften Änderungen.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**PropDesc \_ - \_ Aggregationstyp**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Beschreibt, wie Eigenschaftswerte angezeigt werden, wenn mehrere Elemente ausgewählt werden. Für eine bestimmte Eigenschaft wird der PropDesc- \_ \_ Aggregationstyp beschrieben, wie die-Eigenschaft angezeigt werden soll, wenn mehrere Elemente mit einem Wert für die-Eigenschaft ausgewählt werden, z. b. ob die Werte summiert oder mit einem Mittelwert oder nur mit der Standard Zeichenfolge "Multiple values" angezeigt werden sollen.<br/> |
| [**PropDesc- \_ ColumnIndex- \_ Typ**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Gibt an, ob oder wie eine Eigenschaft indiziert werden kann.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**PropDesc \_ - \_ Bedingungstyp**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | Beschreibt den Bedingungstyp, der beim Anzeigen der Eigenschaft in der Benutzeroberfläche des Abfrage-Generators in Windows Vista verwendet wird, jedoch nicht in Windows 7 und höher.<br/>                                                                                                                                                                                                                                      |
| [**propde- \_ enumfilter**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Beschreibt die gefilterte Liste der Eigenschafts Beschreibungen, die zurückgegeben werden.<br/>                                                                                                                                                                                                                                                                                                          |
| [**PropDesc \_ - \_ Formatflags**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Wird von eigenschaftenbeschreibungs-Hilfsfunktionen wie [**psformatfordisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)verwendet, um das Format einer Eigenschaften Zeichenfolge anzugeben.<br/>                                                                                                                                                                                                                         |
| [**PropDesc \_ relativedescription- \_ Typ**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Beschreibt den relativen Beschreibungs Typ für eine Eigenschafts Beschreibung, wie durch das *relativedescriptiontype* -Attribut des [DisplayInfo](./propdesc-schema-displayinfo.md) -Elements festgelegt.<br/>                                                                                                                                                                                   |
| [**propde- \_ SearchInfo- \_ Flags**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | Bestimmt, ob und wie eine Eigenschaft von Windows Search indiziert wird.<br/>                                                                                                                                                                                                                                                                                                             |
| [**PropDesc \_ - \_ Typflags**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Beschreibt Attribute des [TypeInfo](./propdesc-schema-typeinfo.md) -Elements in der. PropDesc-Datei der Eigenschaft.<br/>                                                                                                                                                                                                                                                                |
| [**propde- \_ \_ ansichtflags**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Diese Flags beschreiben Eigenschaften in den Zeichen folgen der Eigenschaften Beschreibungs Liste.<br/>                                                                                                                                                                                                                                                                                                           |
| [**propertyui- \_ Flags**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Gibt Eigenschafts Funktionen an.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**propvar- \_ Vergleichs \_ Einheit**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Diese Flags sind bestimmten [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur vergleichen zugeordnet.<br/>                                                                                                                                                                                                                                                                               |
| [**PSC- \_ Status**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Gibt den Zustand einer Eigenschaft an. Sie werden manuell durch den Code festgelegt, der den Speicher Cache im Speicher im Speicher gehostet.<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Eigenschaften](props.md)
</dt> <dt>

[Eigenschafts Beschreibungs Schema](property-description-schema.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> <dt>

[Schnittstellen](interfaces.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> <dt>

[Strukturen](structures.md)
</dt> </dl>

 

 
