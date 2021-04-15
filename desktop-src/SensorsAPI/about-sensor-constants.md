---
description: Informationen zu Sensor Konstanten
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: Informationen zu Sensor Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea862d38af74058d11d3a6fa1eb11a702b3b277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529873"
---
# <a name="about-sensor-constants"></a>Informationen zu Sensor Konstanten

Der Windows-Sensor und die Location-Plattform verwenden Konstanten in vielerlei Hinsicht. Die Plattform definiert verschiedene Konstanten, die Sie in Ihrem Sensor Treibercode verwenden können. Sensor Hersteller können benutzerdefinierte Konstanten definieren. Die Definitionen von Platt Form definierten Konstanten finden Sie in der Datei "Sensors. h". Ausführliche Informationen zu Platt Form definierten Sensor Konstanten finden Sie unter [Konstanten](constants.md).

### <a name="sensor-and-data-organization"></a>Sensor-und Datenorganisation

Die Plattform organisiert Sensoren und Daten auf folgende Weise.

-   Kategorien stellen umfassende Klassen von Sensorgeräten dar. Mit Kategorien können Sie Sensoren gruppieren, die wahrscheinlich ähnliche Arten von Informationen bereitstellen oder anderweitig in irgendeiner Weise verknüpft sind. Jede Kategorie wird durch eine **GUID** -Konstante dargestellt. Beispielsweise gehören Sensoren, die breiten-und Längenkoordinaten melden, zur Kategorie der Standort Sensoren. Dies wird durch die \_ Speicherort Konstante der Sensor Kategorie dargestellt \_ .
-   Sensor Typen stellen bestimmte Arten von Sensoren dar. Jeder Sensortyp passt zu einer bestimmten Kategorie. Zwei Sensoren unterschiedlicher Typen können zur gleichen Kategorie oder zu unterschiedlichen Kategorien gehören. Jeder Sensortyp wird durch eine **GUID** -Konstante dargestellt. Beispielsweise wird ein globaler Positionierungssystem Sensor durch die \_ \_ GPS-Konstante des Sensor Typs identifiziert \_ . Ein Sensor, der den aktuellen Speicherort über eine IP-Adresse bereitstellt, wird jedoch durch die \_ Such Konstante des Sensor Typs identifiziert \_ \_ . Beide Sensoren würden jedoch zur Kategorie "Speicherort Sensor" gehören.
-   Datentypen stellen bestimmte Arten von Informationen dar, die der Sensor bereitstellen kann. Sensor Datentypen können den tatsächlichen Messwert enthalten, z. b. die Höhe. Informationen zu den Einheiten, die zum Ausdrücken der Daten verwendet werden, z. b. Meter. und Bezugspunkte für die Daten, wie z. b. die Meeres Ebene. Jeder Datentyp wird durch eine **PropertyKey** -Konstante dargestellt. Beispielsweise wird der-Datentyp, der die Höhe oberhalb der Meeres Ebene in Meter darstellt, durch die Konstante des Sensor \_ \_ Datentyps für \_ Höhen \_ versiegeln identifiziert \_ .
-   Beim Melden von Daten ist ein Wert, der in einem Datenfeld enthalten ist, und eine Sammlung verwandter Datenfelder, die einen Datenbericht bilden. Daten Berichte werden mithilfe der [iportabledebug](/previous-versions//ms740012(v=vs.85)) -Schnittstelle zusammengepackt. Jeder Datenbericht muss mindestens ein gültiges Datenfeld und einen Zeitstempel enthalten, der angibt, wann der Datenbericht erstellt wurde. Zeitstempel werden durch die \_ timestamp-Konstante des Sensor \_ Datentyps dargestellt \_ .

### <a name="other-constants"></a>Andere Konstanten

Das Programm muss auch andere Konstanten verwenden. Diese Konstanten umfassen Folgendes:

-   Sensoreigenschaften, z. b \_ . Beschreibung der Sensor Eigenschaft \_ . In der Regel werden diese Konstanten verwendet, um einen Sensor zu beschreiben. Einige Sensoreigenschaften müssen vom Sensor bereitgestellt werden, einige Eigenschaften können von Client Anwendungen festgelegt werden, und einige müssen immer denselben Wert vom Sensor zurückgeben. Der Abschnitt " [**Sensor Eigenschaften**](sensor-properties.md) Referenz" enthält diese Informationen für jede Eigenschaft.
-   Ereignis Konstanten, z. b \_ . der Sensor Ereignis Status, wurden \_ \_ geändert. Zu den Ereignis Konstanten gehören **GUID** s, die Typen von Ereignissen darstellen, und **PropertyKey** s, die Ereignis Parametertypen darstellen. Diese Konstanten werden für Methodenaufrufe verwendet, z. b. [**iSensor:: seteventinterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) und [**iSensor:: geteventinterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest).

### <a name="custom-constants"></a>Benutzerdefinierte Konstanten

Sensor Hersteller können benutzerdefinierte Konstanten definieren. Beispielsweise kann ein Sensor zu einer Kategorie gehören, die nicht von der Plattform definiert wird. Bevor Sie einen Sensor verwenden können, der benutzerdefinierte Konstanten definiert, muss der Sensorhersteller die Werte veröffentlichen, z. b. durch Veröffentlichen einer Header Datei. Weitere Informationen finden Sie in der Dokumentation, die mit dem Sensor bereitgestellt wird.

 

 
