---
description: Das Sensordatenberichtsobjekt enthält Sensordaten.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Das Sensordatenberichtsobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca1a8e5f61b23753437bd8b1cf4c2a176515b7042b21e84c4d2f431debc8fe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992600"
---
# <a name="the-sensor-data-report-object"></a>Das Sensordatenberichtsobjekt

Das Sensordatenberichtsobjekt enthält Sensordaten.

Damit ein Sensor nützlich ist, muss er aussagekräftige Daten bereitstellen. Die Menge und Häufigkeit der Datengenerierung variiert von Sensor zu Sensor. Beispielsweise würde ein Sensor, der erkennt, ob eine Tür  geöffnet ist, eine kleine Menge boolescher Daten generieren, während ein Bewegungssensor kontinuierlich mehrere Datenelemente generieren kann. Um die Art und Weise zu standardisieren, wie Ihr Programm Daten empfängt, verwendet die Sensor-API das Sensordatenberichtsobjekt.

Sie können über die [**ISensorDataReport-Schnittstelle**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) auf die Informationen in einem Sensordatenbericht zugreifen. Mit dieser Schnittstelle können Sie den Zeitstempel des Datenberichts abrufen, um zu bestimmen, ob die Informationen im Bericht nützlich sind. Sie können die Daten selbst auf zwei Arten abrufen: als einzelner Datenfeldwert oder als Satz von Werten. Um Daten als einzelnen Wert abzurufen, rufen Sie die [**GetSensorValue-Methode**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) auf. Um mehrere Werte abzurufen, rufen Sie die [**GetSensorValues-Methode**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) auf.

Sie geben den Typ der Daten oder Datenfelder an, die Sie mithilfe einer **PROPERTYKEY-Konstante** aus dem Bericht abrufen möchten. Eigenschaftsschlüssel für Datenfelder gängiger Sensortypen werden in Sensors.h definiert.

 

 
