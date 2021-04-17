---
description: Abrufen von Eigenschaften für mehrere Objekte nach Objekt Format
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Abrufen von Eigenschaften für mehrere Objekte nach Objekt Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485459"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>Abrufen von Eigenschaften für mehrere Objekte nach Objekt Format

Zusätzlich zum Massen Abruf von Eigenschaften für eine Auflistung von Objekt bezeichmern kann eine Anwendung auch einen Massen Abruf von Eigenschaften für alle Objekte eines bestimmten Typs durchführen. Wie im vorherigen Beispiel ist es für den Massen Abruf für einen bestimmten Typ erforderlich, dass der Gerätetreiber Massen Abruf Vorgänge unterstützt.

Die Anwendung kann einen Massen Abruf mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen ausführen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.                   |
| [**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)                 | Wird verwendet, um die abzurufenden Eigenschaften zu identifizieren.                   |
| [**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Wird verwendet, um zu bestimmen, ob ein bestimmter Treiber Massen Vorgänge unterstützt. |
| [**Iportabledevicepropertiesbulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Unterstützt den Massen Abruf Vorgang.                             |
| [**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Speichern der Objekt Bezeichner für den Massen Vorgang verwendet.       |



 

Die Funktion "lesecontentpropertiesbulkfilteringformat" im Modul "contentproperties. cpp" der Beispielanwendung veranschaulicht einen Massen Abruf Vorgang für Objekte eines bestimmten Typs oder Formats.

Der Code in der Funktion "Read contentpropertiesbulkfilteringformat" ist nahezu identisch mit dem Code, der in der Funktion "Read contentpropertiesbulk" gefunden wurde. (Eine ausführliche Beschreibung dieser Funktion finden Sie im Thema [Abrufen von Eigenschaften für mehrere Objekte](retrieving-properties-for-multiple-objects.md) .)

Der einzige Hauptunterschied tritt auf, wenn der Vorgang in die Warteschlange eingereiht wird. Beim Filtern nach Typ oder Format wird die [**iportabledevicepropertiesbulk:: queuegetvaluesbyobjectformat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) -Methode anstelle der [**iportabledevicepropertiesbulk:: queuegetvaluesbyobjectlist**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) -Methode aufgerufen.


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Iportabledevicepropertiesbulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



