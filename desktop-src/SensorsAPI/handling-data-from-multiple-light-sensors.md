---
description: Verwenden von Licht Sensor Daten
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Verwenden von Licht Sensor Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccf1c032b4100174afd6073d8c43db27bce3892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353858"
---
# <a name="using-light-sensor-data"></a>Verwenden von Licht Sensor Daten

Es gibt zwei empfohlene Methoden zum Interpretieren und Verwenden von Lux-Daten, die von Umgebungslichtsensoren stammen.

-   Wenden Sie eine Transformation auf die Daten an, sodass die normalisierte Lichtebene direkt im Verhältnis zu Programmverhalten oder Interaktionen verwendet werden kann. Ein Beispiel wäre das Ändern der Größe einer Schaltfläche in Ihrem Programm in direktem Verhältnis zu den normalisierten Daten (oder einem Bereich der normalisierten Daten, z.b. für die Einstellung "Outdoor"). Dieser Ansatz bietet die optimale Implementierung.
-   Behandeln Sie Bereiche von Lux-Daten, und ordnen Sie Programmverhalten und Reaktionen auf den oberen und unteren Schwellenwert dieser Bereiche von Lux-Daten zu. Dies ist eine einfache Möglichkeit, auf Beleuchtungsbedingungen zu reagieren, und bietet möglicherweise nicht die optimale Benutzer Leistung. Diese Vorgehensweise funktioniert jedoch problemlos, wenn reibungslose Übergänge nicht möglich sind.

## <a name="handling-data-from-multiple-light-sensors"></a>Verarbeiten von Daten aus mehreren Lichtsensoren

Um die präzisere Näherung der aktuellen Beleuchtungsbedingungen zu erreichen, können Sie Daten aus mehreren Umgebungslichtsensoren verwenden. Da Ambient-Light-Sensoren teilweise oder vollständig durch Schatten oder Objekte verdeckt werden können, die den Sensor abdecken, können mehrere Sensoren, die eine gewisse Entfernung aufweisen, eine viel bessere Näherung der aktuellen Beleuchtungsbedingungen darstellen als ein einzelner Sensor.

Um die Daten zu verfolgen, die von mehreren Sensoren stammen, können Sie die folgenden beiden Methoden verwenden:

-   Der aktuellste Datenwert für jeden Umgebungslichtsensor kann zusammen mit dem Zeitstempel des Sensordaten Berichts für jede dieser Messwerte beibehalten werden. Der letzte für jeden Sensor Lesevorgang empfangene " [**isensordatareport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) " konnte beibehalten werden und kann beide Werte für einen späteren Verweis enthalten. Durch den Verweis auf den Zeitstempel für die einzelnen Sensordaten Berichte können die Daten basierend auf dem Alter verwaltet werden. Wenn die Daten z. b. mehr als 2 Sekunden alt sind, können Sie ausgelassen werden. Basierend auf den neueren Sensordaten Werten könnte die höchste Lese barkeit verwendet werden, da der entsprechende Sensor vermutlich nicht verdeckt wäre.
-   Sie können den zuletzt gemeldeten Umgebungslichtsensor-Wert verwenden. Diese Implementierung wäre nicht optimal, da die Werte von mehreren Sensoren nicht miteinander verglichen werden, um das genaueste Ergebnis zu erhalten. Diese Methode wird nicht empfohlen.

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode zeigt eine Implementierung für das [**ondataupdatiert**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) -Ereignis. Der Ereignishandler ruft eine Hilfsfunktion mit dem Namen **UpdateUI** auf, die die Benutzeroberfläche basierend auf dem Lux-Wert ändert. Wenn Sie die Implementierung von UpdateUI schreiben, sind Sie auf dem neuesten Stand.


```C++
// Override of ISensorEvents::OnDataUpdated
// Part of an event sink implementation for ISensorEvents
STDMETHODIMP CALSEventSink::OnDataUpdated(
    ISensor* pSensor, 
    ISensorDataReport* pNewData)
{
    HRESULT hr = S_OK;
   
    if(pSensor == NULL ||
       pNewData == NULL)
    {
         return E_POINTER;
    }

    // Declare and initialize the PROPVARIANT
    PROPVARIANT lightLevel;
    PropVariantInit(&lightLevel);

    // Get the sensor reading from the ISensorDataReport object
    hr = pNewData->GetSensorValue(
        SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX, 
        &lightLevel);

    if(SUCCEEDED(hr))
    {
        if(lightlevel.vt == VT_R4)
        {
            // Extract the float value from the PROPVARIANT object
            float luxValue = lightLevel.fltVal;

            // Normalize the light sensor data
            double lightNormalized = ::log10(luxValue) / 5.0;

            // Handle UI changes based on the normalized LUX data
            // which ranges from 0.0 - 1.0 for a lux range of 
            // 0 lux to 100,000 lux. 
            UpdateUI(lightNormalized);
        }
    }

    // Release the variant.     
    PropVariantClear(&lightLevel);

    return hr;
}
```



 

 
