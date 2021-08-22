---
description: Informationen zu Sensorkonstanten
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: Informationen zu Sensorkonstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cab8b5def4cdfa185a55dd993896fb5157563424b7753497413e5d7706465e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890255"
---
# <a name="about-sensor-constants"></a>Informationen zu Sensorkonstanten

Die Windows Sensor- und Standortplattform verwendet Konstanten in vielerlei Hinsicht. Die Plattform definiert verschiedene Konstanten, die Sie in Ihrem Sensortreibercode verwenden können. Sensorhersteller können benutzerdefinierte Konstanten definieren. Die Definitionen von plattformdefinierte Konstanten finden Sie in der Datei Sensors.h. Ausführliche Informationen zu plattformdefinierte Sensorkonstanten finden Sie unter [Konstanten.](constants.md)

### <a name="sensor-and-data-organization"></a>Sensor- und Datenorganisation

Die Plattform organisiert Sensoren und Daten auf folgende Weise.

-   Kategorien stellen breite Klassen von Sensorgeräten dar. MitHilfe von Kategorien können Sie Sensoren gruppieren, die wahrscheinlich ähnliche Arten von Informationen bereitstellen oder anderweitig in irgendeiner Weise miteinander verknüpft sind. Jede Kategorie wird durch eine **GUID-Konstante** dargestellt. Beispielsweise gehören Sensoren, die Breiten- und Längenkoordinaten melden, zur Kategorie des Standortsensors. Dies wird durch die \_ SENSOR CATEGORY \_ LOCATION-Konstante dargestellt.
-   Sensortypen stellen bestimmte Arten von Sensoren dar. Jeder Sensortyp passt in eine bestimmte Kategorie. Zwei Sensoren unterschiedlicher Typen können derselben Kategorie oder unterschiedlichen Kategorien angehören. Jeder Sensortyp wird durch eine **GUID-Konstante** dargestellt. Beispielsweise wird ein globaler Positionierungssystemsensor durch die GPS-Konstante SENSOR \_ TYPE \_ LOCATION \_ identifiziert. Ein Sensor, der den aktuellen Standort mithilfe einer IP-Adresse bereitstellt, wird jedoch durch die \_ \_ LOOKUP-Konstante SENSOR TYPE LOCATION \_ identifiziert. Beide Sensoren gehören jedoch zur Kategorie Standortsensor.
-   Datentypen stellen bestimmte Arten von Informationen dar, die der Sensor bereitstellen kann. Sensordatentypen können den tatsächlichen Messwert enthalten, z. B. Höhe; Informationen zu den Einheiten, die zum Ausdrücken der Daten verwendet werden, z. B. Meter; und Verweispunkte für die Daten, z. B. den Seegrad. Jeder Datentyp wird durch eine **PROPERTYKEY-Konstante** dargestellt. Beispielsweise wird der Datentyp, der die Höhe über dem Wasserstand in Metern darstellt, durch die KONSTANTE SENSOR \_ DATA \_ TYPE ALTITUDE \_ \_ SEALEVEL METERS \_ identifiziert.
-   Beim Melden von Daten wird ein Wert als in einem Datenfeld enthalten bezeichnet, und eine Sammlung verwandter Datenfelder besteht aus einem Datenbericht. Datenberichte werden mithilfe der [IPortableDeviceValues-Schnittstelle](/previous-versions//ms740012(v=vs.85)) gepackt. Jeder Datenbericht muss mindestens ein gültiges Datenfeld und einen Zeitstempel enthalten, der angibt, wann der Datenbericht erstellt wurde. Zeitstempel werden durch die \_ \_ TIMESTAMP-Konstante SENSOR DATA TYPE \_ dargestellt.

### <a name="other-constants"></a>Andere Konstanten

Das Programm muss auch andere Konstanten verwenden. Diese Konstanten umfassen Folgendes:

-   Sensoreigenschaften, z. B. SENSOR \_ PROPERTY \_ DESCRIPTION. Normalerweise werden diese Konstanten verwendet, um einen Sensor zu beschreiben. Einige Sensoreigenschaften müssen vom Sensor bereitgestellt werden, einige Eigenschaften können von Clientanwendungen festgelegt werden, und einige müssen immer den gleichen Wert vom Sensor zurückgeben. Der Referenzabschnitt [**Sensoreigenschaften**](sensor-properties.md) enthält diese Informationen für jede Eigenschaft.
-   Ereigniskonstanten, z. B. SENSOR \_ EVENT \_ STATE \_ CHANGED. Zu den Ereigniskonstanten gehören **GUID** s, die Ereignistypen darstellen, und **PROPERTYKEY** s, die Ereignisparametertypen darstellen. Sie verwenden diese Konstanten für Methodenaufrufe, z.B. [**ISensor::SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) und [**ISensor::GetEventInterest.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest)

### <a name="custom-constants"></a>Benutzerdefinierte Konstanten

Sensorhersteller können benutzerdefinierte Konstanten definieren. Beispielsweise kann ein Sensor zu einer Kategorie gehören, die nicht von der Plattform definiert ist. Bevor Sie einen Sensor verwenden können, der benutzerdefinierte Konstanten definiert, muss der Sensorhersteller die Werte veröffentlichen, z. B. durch Veröffentlichen einer Headerdatei. Weitere Informationen finden Sie in der Dokumentation, die mit dem Sensor bereitgestellt wird.

 

 
