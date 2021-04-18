---
description: Zugreifen auf Dienst Objekteigenschaften
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Zugreifen auf Dienst Objekteigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347152"
---
# <a name="accessing-service-object-properties"></a>Zugreifen auf Dienst Objekteigenschaften

Eine Anwendung kann Eigenschaften für ein einzelnes Objekt in einem Dienst, für mehrere Objekte, die durch Objekt Bezeichner oder für mehrere Objekte desselben Typs identifiziert werden, lesen und schreiben. Das Thema " [Abrufen von Objekteigenschaften](retrieving-content-object-properties.md) " beschreibt das Lesen von Eigenschaften für ein einzelnes Objekt in einem Dienst. Das Thema [Schreiben von Objekteigenschaften](writing-content-object-properties.md) beschreibt das Schreiben von Eigenschaften für ein einzelnes Objekt in einem Dienst.

Weitere Informationen zum Abrufen von Eigenschaften für mehrere Objekte finden Sie im Abschnitt " [Erweiterte Aufgaben](advanced-tasks.md) ".

## <a name="when-to-use-service-property-definitions"></a>Verwendungszwecke von Dienst Eigenschafts Definitionen

Die WPD-API-Aufrufe zum Abrufen und Festlegen von Objekteigenschaften für einen Dienst sind identisch mit den Aufrufen zum Abrufen von Objekteigenschaften für ein Gerät (Vergleich "Abrufen von Eigenschaften für ein einzelnes Objekt"). Der Hauptunterschied besteht darin, dass ein anderer Satz von PropertyKeys verwendet wird, um Objekteigenschaften abzufragen. Für wpdserviceapisample werden Geräte Dienst-PropertyKeys verwendet (z. **b. pkey \_ Generika \_ Name**); für wpdapisample werden WPD PropertyKeys (z. b. **WPD- \_ Objekt \_ Name**) verwendet.

Die Eigenschafts Schlüssel für den Geräte Dienst sind in bridgedeviceservices. h (enthalten in jeder Dienst Header Datei) definiert und stellen den gemeinsamen Satz von PropertyKeys dar, die sowohl von Geräte Dienst Anwendungen als auch von der Firmware-Implementierung auf dem Gerät verwendet werden. Dies ermöglicht einen konsistenten Satz von Definitionen im gesamten Geräte Stapel mit minimaler Übersetzung, gruppiert PropertyKeys auf der Grundlage des Diensts und ermöglicht das einfache Definieren neuer Dienste, ohne das WPD-Schema aktualisieren zu müssen.

Der verwendete Satz von PropertyKeys hängt von den Anforderungen der Anwendung ab:

-   Wenn Ihre Anwendung mit dem Gerät durch Aufrufen von [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)kommuniziert, verwenden Sie die in portabledevice. h definierten PropertyKeys. Ein Beispiel für eine solche Anwendung ist wpdapisample.
-   Wenn Ihre Anwendung mit den Geräte Diensten kommuniziert, indem Sie [**iportabledeviceservice:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)aufrufen, verwenden Sie die in bridgedeviceservices. h definierten PropertyKeys. Ein Beispiel für eine solche Anwendung ist wpdservicesapisample.
-   Wenn Sie eine komplexe Anwendung schreiben, die eine Hybrid Geräte Dienste und ein Gerät unterstützen muss (Dies bedeutet, dass Ihre Anwendung beide **iportabledevice** -Befehle aufruft: Open und **iportabledeviceservice:: Open**) Sie müssen die WPD PropertyKeys verwenden, wenn Sie iportabledevice und seine abgeleiteten Schnittstellen und den Geräte Dienst PropertyKeys verwenden, wenn Sie [iportabledeviceservice](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) und seine abgeleiteten Schnittstellen verwenden.

Die meisten WPD-Anwendungen sollten in die erste oder zweite Kategorie fallen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**Iportabledeviceproperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[Abrufen von Objekteigenschaften](retrieving-content-object-properties.md)
</dt> <dt>

[Schreiben von Objekteigenschaften](writing-content-object-properties.md)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



