---
description: In diesem Abschnitt werden die Windows, Enumerationen und Flags des Eigenschaftensystems beschrieben.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: Konstanten, Enumerationen und Flags (Windows-Eigenschaftensystem)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e39d357ae741ae49c4fa98c886e8c08b3594a2ea3a7e4e045def96abe8c2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718209"
---
# <a name="constants-enumerations-and-flags"></a>Konstanten, Enumerationen und Flags

In diesem Abschnitt werden die Windows, Enumerationen und Flags des Eigenschaftensystems beschrieben.



| Thema                                                                              | Inhalte                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Gibt Flags an, die das Eigenschaftenspeicherobjekt ändern, das von Methoden abgerufen wurde, die einen Eigenschaftenspeicher erstellen, z.B. [**IShellItem2::GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) oder [**IPropertyStoreFactory::GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Stellt Vorgangsstatusflags zurEntspricht.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**\_PKA-FLAGS**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Beschreibt das Verhalten des Eigenschaftenänderungsarrays.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_PROPDESC-AGGREGATIONSTYP \_**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Beschreibt, wie Eigenschaftswerte angezeigt werden, wenn mehrere Elemente ausgewählt werden. Für eine bestimmte Eigenschaft beschreibt PROPDESC AGGREGATION TYPE, wie die Eigenschaft angezeigt werden soll, wenn mehrere Elemente mit einem Wert für die Eigenschaft ausgewählt werden, z. B. ob die Werte summiert oder gemittelt oder einfach mit der Standardzeichenfolge \_ \_ "Mehrere Werte" angezeigt werden sollen.<br/> |
| [**PROPDESC \_ \_ COLUMNINDEX-TYP**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Gibt an, ob oder wie eine Eigenschaft indiziert werden kann.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**\_PROPDESC-BEDINGUNGSTYP \_**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | Beschreibt den Bedingungstyp, der beim Anzeigen der Eigenschaft in der Benutzeroberfläche des Abfrage-Generators in Windows Vista verwendet werden soll, jedoch nicht in Windows 7 und höher.<br/>                                                                                                                                                                                                                                      |
| [**PROPDESC \_ ENUMFILTER**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Beschreibt die gefilterte Liste der zurückgegebenen Eigenschaftenbeschreibungen.<br/>                                                                                                                                                                                                                                                                                                          |
| [**\_PROPDESC-FORMATFLAGS \_**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Wird von Hilfsfunktionen für Eigenschaftenbeschreibungen wie [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)verwendet, um das Format einer Eigenschaftenzeichenfolge anzugeben.<br/>                                                                                                                                                                                                                         |
| [**PROPDESC \_ \_ RELATIVEDESCRIPTION-TYP**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Beschreibt den relativen Beschreibungstyp für eine Eigenschaftenbeschreibung, wie durch das *relativeDescriptionType-Attribut* des [displayInfo-Elements](./propdesc-schema-displayinfo.md) bestimmt.<br/>                                                                                                                                                                                   |
| [**PROPDESC \_ \_ SEARCHINFO-FLAGS**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | Bestimmt, ob und wie eine Eigenschaft durch Die Suche Windows wird.<br/>                                                                                                                                                                                                                                                                                                             |
| [**\_PROPDESC-TYPFLAGS \_**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Beschreibt Attribute des [typeInfo-Elements](./propdesc-schema-typeinfo.md) in der PROPDESC-Datei der Eigenschaft.<br/>                                                                                                                                                                                                                                                                |
| [**\_ \_ PROPDESC-ANSICHTSFLAGS**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Diese Flags beschreiben Eigenschaften in Eigenschaftenbeschreibungslisten-Zeichenfolgen.<br/>                                                                                                                                                                                                                                                                                                           |
| [**\_PROPERTYUI-FLAGS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Gibt Eigenschaftenfeatures an.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**\_PROPVAR-VERGLEICHSEINHEIT \_**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Diese Flags sind bestimmten [**PROPVARIANT-Strukturvergleichen**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) zugeordnet.<br/>                                                                                                                                                                                                                                                                               |
| [**\_PSC-STATUS**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Gibt den Zustand einer Eigenschaft an. Sie werden manuell durch den Code festgelegt, der den In-Memory-Eigenschaftenspeichercache hosten soll.<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Eigenschaften](props.md)
</dt> <dt>

[Schema der Eigenschaftenbeschreibung](property-description-schema.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> <dt>

[Schnittstellen](interfaces.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> <dt>

[Strukturen](structures.md)
</dt> </dl>

 

 
