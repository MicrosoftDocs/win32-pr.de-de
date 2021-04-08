---
description: Das Sensordaten-Berichts Objekt enthält Sensordaten.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Das Datenberichts Objekt des Sensors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d43753aa28be5cd20c85b7e65bf4c7516d4c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960119"
---
# <a name="the-sensor-data-report-object"></a>Das Datenberichts Objekt des Sensors

Das Sensordaten-Berichts Objekt enthält Sensordaten.

Damit ein Sensor nützlich ist, muss er sinnvolle Daten bereitstellen. Der Umfang und die Häufigkeit der Datengenerierung variieren vom Sensor zum Sensor. Beispielsweise würde ein Sensor, der erkennt, ob eine Tür geöffnet ist, eine kleine Menge an **booleschen** Daten generieren, während ein Bewegungssensor ständig mehrere Datenelemente generieren kann. Zum standardisieren der Art und Weise, in der das Programm Daten empfängt, verwendet die Sensor-API das Sensordaten-Berichts Objekt.

Sie können auf die Informationen in einem Sensordaten Bericht über die Schnittstelle " [**isensordatareport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) " zugreifen. Mit dieser Schnittstelle können Sie den Zeitstempel des Datenberichts abrufen, damit Sie bestimmen können, ob die Informationen im Bericht nützlich sind. Sie können die Daten auf zweierlei Weise abrufen: als einzelner Daten Feldwert oder als Satz von Werten. Zum Abrufen von Daten als einzelner Wert rufen Sie die [**getsensorvalue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) -Methode auf. Rufen Sie die [**getsensorvalues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) -Methode auf, um mehrere Werte abzurufen.

Sie geben den Typ der Daten oder Datenfelder an, die Sie aus dem Bericht abrufen möchten, indem Sie eine **PropertyKey** -Konstante verwenden. Eigenschafts Schlüssel für Datenfelder allgemeiner Sensortypen werden in "Sensors. h" definiert.

 

 
