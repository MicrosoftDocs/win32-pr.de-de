---
description: In diesem Abschnitt werden die System Schnittstellen von Windows-Eigenschaften beschrieben.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Schnittstellen (Windows-Eigenschaften System)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5003458683fb9b2443df0301676b601901817d54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367961"
---
# <a name="interfaces-windows-property-system"></a>Schnittstellen (Windows-Eigenschaften System)

In diesem Abschnitt werden die System Schnittstellen von Windows-Eigenschaften beschrieben.



| Thema                                                                                        | Inhalte                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Macht eine Methode verfügbar, die eine Änderung an einer einzelnen Eigenschaft kapselt.                                                                                                                                                                                                                                                                                                                          |
| [**Ipropertychangearray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Macht Methoden für mehrere mehrere Änderungs Vorgänge verfügbar, die an [**IFileOperation**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation)übermittelt werden können.                                                                                                                                                                                                                                                                   |
| [**Ipropertydescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Macht Methoden verfügbar, die Details zu einzelnen Eigenschafts Beschreibungen aufzählen und abrufen.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Macht Methoden verfügbar, die Details zu einzelnen Eigenschafts Beschreibungen aufzählen und abrufen.                                                                                                                                                                                                                                                                                                       |
| [**Ipropertydescriptionaliasinfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Macht Methoden verfügbar, um die Spalten Eigenschaften "Sortieren nach" für ein Element zu erhalten. Diese Schnittstelle wird von UI-Objekten verwendet, die die primären oder sekundären Sortier Spalten für eine bestimmte Eigenschaft abrufen möchten.                                                                                                                                                                                                |
| [**Ipropertydescriptionlist**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Macht Methoden verfügbar, die Informationen aus einer Auflistung von Eigenschafts Beschreibungen extrahieren, die als Liste dargestellt werden.                                                                                                                                                                                                                                                                                   |
| [**Ipropertydescriptionrelatedpropertyinfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Stellt eine Methode bereit, die eine [**ipropertydescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) -Schnittstelle abruft.                                                                                                                                                                                                                                                                                       |
| [**Ipropertydescriptionsearchinfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Macht suchbezogene Informationen für eine Eigenschaft verfügbar. Die von dieser Schnittstelle bereitgestellten Informationen stammen aus dem [propertydescription](./propdesc-schema-propertydescription.md) -Schema, dem [SearchInfo](./propdesc-schema-searchinfo.md) -Element für eine bestimmte Eigenschaft. Diese Informationen werden vom Windows Search-Indexer verwendet. Die meisten aufrufenden Anwendungen müssen diese Schnittstelle nicht aufrufen. |
| [**Ipropertyenumtype**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Macht Methoden verfügbar, mit denen Daten aus enumerationsinformationen extrahiert werden. [**Ipropertyenumtype**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) ermöglicht zur Laufzeit auf programmgesteuerte Weise den Zugriff auf die Enumerationselemente [und die](./propdesc-schema-enum.md) [enumrange](./propdesc-schema-enumrange.md) -Elemente im [Eigenschafts Schema](./propdesc-schema-entry.md) .                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Macht Methoden verfügbar, mit denen Daten aus enumerationsinformationen extrahiert werden. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) erweitert [**ipropertyenumtype**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype).                                                                                                                                                                                                               |
| [**Ipropertyenumtypelist**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Macht Methoden verfügbar, mit denen die möglichen Werte für eine Eigenschaft aufgelistet werden.                                                                                                                                                                                                                                                                                                                         |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Macht Methoden zum Auflisten, zum erhalten und Festlegen von Eigenschafts Werten verfügbar.                                                                                                                                                                                                                                                                                                                     |
| [**Ipropertystorecache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Macht Methoden verfügbar, die es einem Handler ermöglichen, verschiedene Zustände für jede Eigenschaft zu verwalten.                                                                                                                                                                                                                                                                                                           |
| [**Ipropertystorecapabilitäten**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Macht eine Methode verfügbar, die bestimmt, ob eine Eigenschaft vom Benutzer in der Benutzeroberfläche bearbeitet werden kann.                                                                                                                                                                                                                                                                                                   |
| [**Ipropertystorefactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Macht Methoden zum Aufrufen eines [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts verfügbar.                                                                                                                                                                                                                                                                                                               |
| [**Ipropertysystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Macht Methoden verfügbar, die Eigenschafts Beschreibungen erhalten, Eigenschafts Schemas registrieren und deren Registrierung aufheben, Eigenschafts Beschreibungen aufzählen und Eigenschaftswerte auf typstrikte Weise formatieren.                                                                                                                                                                                                                |
| [**Ipropertyui**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Entwickler sollten stattdessen [**ipropertydescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) verwenden.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Eigenschaften](props.md)
</dt> <dt>

[Eigenschafts Beschreibungs Schema](property-description-schema.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> <dt>

[Strukturen](structures.md)
</dt> <dt>

[Konstanten, Enumerationen und Flags](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
