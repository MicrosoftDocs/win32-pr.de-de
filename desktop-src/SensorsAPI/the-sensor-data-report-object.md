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
# <a name="the-sensor-data-report-object"></a><span data-ttu-id="bc004-103">Das Datenberichts Objekt des Sensors</span><span class="sxs-lookup"><span data-stu-id="bc004-103">The Sensor Data Report Object</span></span>

<span data-ttu-id="bc004-104">Das Sensordaten-Berichts Objekt enthält Sensordaten.</span><span class="sxs-lookup"><span data-stu-id="bc004-104">The sensor data report object contains sensor data.</span></span>

<span data-ttu-id="bc004-105">Damit ein Sensor nützlich ist, muss er sinnvolle Daten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bc004-105">For a sensor to be useful, it must provide meaningful data.</span></span> <span data-ttu-id="bc004-106">Der Umfang und die Häufigkeit der Datengenerierung variieren vom Sensor zum Sensor.</span><span class="sxs-lookup"><span data-stu-id="bc004-106">The amount and frequency of data generation varies from sensor to sensor.</span></span> <span data-ttu-id="bc004-107">Beispielsweise würde ein Sensor, der erkennt, ob eine Tür geöffnet ist, eine kleine Menge an **booleschen** Daten generieren, während ein Bewegungssensor ständig mehrere Datenelemente generieren kann.</span><span class="sxs-lookup"><span data-stu-id="bc004-107">For example, a sensor that detects whether a door is open would generate a small amount of **Boolean** data, while a motion sensor might continuously generate multiple data items.</span></span> <span data-ttu-id="bc004-108">Zum standardisieren der Art und Weise, in der das Programm Daten empfängt, verwendet die Sensor-API das Sensordaten-Berichts Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc004-108">To standardize the way your program receives data, the Sensor API uses the sensor data report object.</span></span>

<span data-ttu-id="bc004-109">Sie können auf die Informationen in einem Sensordaten Bericht über die Schnittstelle " [**isensordatareport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) " zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bc004-109">You can access the information in a sensor data report through the [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) interface.</span></span> <span data-ttu-id="bc004-110">Mit dieser Schnittstelle können Sie den Zeitstempel des Datenberichts abrufen, damit Sie bestimmen können, ob die Informationen im Bericht nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="bc004-110">This interface lets you retrieve the data report's time stamp so that you can determine whether the information in the report is useful.</span></span> <span data-ttu-id="bc004-111">Sie können die Daten auf zweierlei Weise abrufen: als einzelner Daten Feldwert oder als Satz von Werten.</span><span class="sxs-lookup"><span data-stu-id="bc004-111">You can retrieve the data itself in two ways: as an individual data field value or as a set of values.</span></span> <span data-ttu-id="bc004-112">Zum Abrufen von Daten als einzelner Wert rufen Sie die [**getsensorvalue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="bc004-112">To retrieve data as an individual value, call the [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) method.</span></span> <span data-ttu-id="bc004-113">Rufen Sie die [**getsensorvalues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) -Methode auf, um mehrere Werte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc004-113">To retrieve multiple values, call the [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) method.</span></span>

<span data-ttu-id="bc004-114">Sie geben den Typ der Daten oder Datenfelder an, die Sie aus dem Bericht abrufen möchten, indem Sie eine **PropertyKey** -Konstante verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc004-114">You specify the type of data, or data fields, that you want to retrieve from the report by using a **PROPERTYKEY** constant.</span></span> <span data-ttu-id="bc004-115">Eigenschafts Schlüssel für Datenfelder allgemeiner Sensortypen werden in "Sensors. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="bc004-115">Property keys for data fields of common sensor types are defined in Sensors.h.</span></span>

 

 
