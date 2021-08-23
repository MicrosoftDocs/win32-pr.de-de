---
description: In diesem Abschnitt werden die Windows Eigenschaftensystemschnittstellen beschrieben.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Schnittstellen (Windows-Eigenschaftensystem)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d608e1b994541667847d755e95966b6ea2770c2d0c73ce86ef8fbd79b8c9dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600120"
---
# <a name="interfaces-windows-property-system"></a>Schnittstellen (Windows-Eigenschaftensystem)

In diesem Abschnitt werden die Windows Eigenschaftensystemschnittstellen beschrieben.



| Thema                                                                                        | Inhalte                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Macht eine Methode verfügbar, die eine Änderung an einer einzelnen Eigenschaft kapselt.                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Macht Methoden für mehrere Änderungsvorgänge verfügbar, die an [**IFileOperation**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation)übergeben werden können.                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Macht Methoden verfügbar, die Details zu einzelnen Eigenschaftenbeschreibungen aufzählen und abrufen.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Macht Methoden verfügbar, die Details zu einzelnen Eigenschaftenbeschreibungen aufzählen und abrufen.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Macht Methoden verfügbar, um die Spalteneigenschaften "sortieren nach" für ein Element abzurufen. Diese Schnittstelle wird von Benutzeroberflächenobjekten verwendet, die die primären oder sekundären Sortierspalten für eine bestimmte Eigenschaft abrufen möchten.                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Macht Methoden verfügbar, die Informationen aus einer Auflistung von Eigenschaftenbeschreibungen extrahieren, die als Liste dargestellt werden.                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Stellt eine Methode bereit, die eine [**IPropertyDescription-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) wiederholt.                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Macht suchbezogene Informationen für eine Eigenschaft verfügbar. Die von dieser Schnittstelle bereitgestellten Informationen stammen aus dem [propertyDescription-Schema,](./propdesc-schema-propertydescription.md) [dem searchInfo-Element](./propdesc-schema-searchinfo.md) für eine bestimmte Eigenschaft. Diese Informationen werden vom Windows Search Indexer verwendet. Die meisten aufrufenden Anwendungen müssen diese Schnittstelle nicht aufrufen. |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Macht Methoden verfügbar, die Daten aus Enumerationsinformationen extrahieren. [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) ermöglicht den programmgesteuerten Zugriff auf die [Enumerations-](./propdesc-schema-enum.md) und [enumRange-Elemente](./propdesc-schema-enumrange.md) im [Eigenschaftenschema](./propdesc-schema-entry.md) zur Laufzeit.                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Macht Methoden verfügbar, die Daten aus Enumerationsinformationen extrahieren. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) erweitert [**IPropertyEnumType.**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Macht Methoden verfügbar, die die möglichen Werte für eine Eigenschaft aufzählen.                                                                                                                                                                                                                                                                                                                         |
| [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Macht Methoden zum Aufzählen, Abrufen und Festlegen von Eigenschaftswerten verfügbar.                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Macht Methoden verfügbar, mit denen ein Handler verschiedene Zustände für jede Eigenschaft verwalten kann.                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Macht eine Methode verfügbar, die bestimmt, ob eine Eigenschaft vom Benutzer auf der Benutzeroberfläche bearbeitet werden kann.                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Macht Methoden zum Abrufen eines [**IPropertyStore-Objekts**](/windows/win32/api/propsys/nn-propsys-ipropertystore) verfügbar.                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Macht Methoden verfügbar, die Eigenschaftenbeschreibungen abrufen, Eigenschaftenschemas registrieren und deren Registrierung aufheben, Eigenschaftenbeschreibungen aufzählen und Eigenschaftswerte typsicher formatieren.                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Entwickler sollten stattdessen [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) verwenden.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Eigenschaften](props.md)
</dt> <dt>

[Eigenschaftenbeschreibungsschema](property-description-schema.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> <dt>

[Strukturen](structures.md)
</dt> <dt>

[Konstanten, Enumerationen und Flags](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
