---
description: Abrufen von Eigenschaften für mehrere Objekte nach Objektformat
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Abrufen von Eigenschaften für mehrere Objekte nach Objektformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054e06d4f6dbfe13c3c0efad517a6e80d41b5387c8e8cc1b6d2712f3c238a08e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027029"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>Abrufen von Eigenschaften für mehrere Objekte nach Objektformat

Zusätzlich zum Massenabruf von Eigenschaften für eine Auflistung von Objektbezeichnern kann eine Anwendung auch einen Massenabruf von Eigenschaften für alle Objekte eines bestimmten Typs ausführen. Wie im vorherigen Beispiel erfordert der Massenabruf für einen bestimmten Typ, dass der Gerätetreiber Massenabrufe unterstützt.

Ihre Anwendung kann mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen einen Massenabruf durchführen.



| Schnittstelle                                                                                      | Beschreibung                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Ermöglicht den Zugriff auf die inhaltsspezifischen Methoden.                   |
| [**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)                 | Wird verwendet, um die abzurufenden Eigenschaften zu identifizieren.                   |
| [**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Wird verwendet, um zu bestimmen, ob ein angegebener Treiber Massenvorgänge unterstützt. |
| [**IPortableDevicePropertiesBulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Unterstützt den Massenabrufvorgang.                             |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird verwendet, um die Objektbezeichner für den Massenvorgang zu speichern.       |



 

Die ReadContentPropertiesBulkFilteringFormat-Funktion im ContentProperties.cpp-Modul der Beispielanwendung veranschaulicht einen Massenabrufvorgang für Objekte eines bestimmten Typs oder Formats.

Der In der ReadContentPropertiesBulkFilteringFormat-Funktion gefundene Code ist fast identisch mit dem Code in der ReadContentPropertiesBulk-Funktion. (Eine vollständige Beschreibung dieser Funktion finden Sie im Thema Abrufen von [Eigenschaften für mehrere Objekte.)](retrieving-properties-for-multiple-objects.md)

Der einzige Hauptunterschied tritt auf, wenn der Vorgang in die Warteschlange eingereiht wird. Beim Filtern nach Typ oder Format wird die [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) anstelle der [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) aufgerufen.


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

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**IPortableDevicePropertiesBulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



