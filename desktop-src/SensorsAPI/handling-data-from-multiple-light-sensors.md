---
description: Verwenden von Lichtsensordaten
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Verwenden von Lichtsensordaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae4f7047301c7d31d18014bb09512d1f3944c418a34c153a87c001f95fb63a8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425128"
---
# <a name="using-light-sensor-data"></a>Verwenden von Lichtsensordaten

Es gibt zwei empfohlene Methoden zum Interpretieren und Verwenden von Lux-Daten, die von Umgebungslichtsensoren stammen.

-   Wenden Sie eine Transformation auf die Daten an, damit der normalisierte Lichtpegel direkt im Verhältnis zum Programmverhalten oder zu Interaktionen verwendet werden kann. Ein Beispiel wäre, die Größe einer Schaltfläche in Ihrem Programm in direktem Verhältnis zu den normalisierten Daten (oder einem Bereich der normalisierten Daten, z. B. im Freien) zu variieren. Dieser Ansatz bietet die optimale Implementierung.
-   Behandeln Sie Bereiche von Lux-Daten, und ordnen Sie das Verhalten und die Reaktionen des Programms den oberen und unteren Schwellenwerten dieser Lux-Datenbereiche zu. Dies ist eine einfache Möglichkeit, auf Beleuchtungsbedingungen zu reagieren, und führt möglicherweise nicht zu einer optimalen Benutzererfahrung. Dieser Ansatz funktioniert jedoch gut, wenn reibungslose Übergänge nicht möglich sind.

## <a name="handling-data-from-multiple-light-sensors"></a>Verarbeiten von Daten von mehreren Lichtsensoren

Um die genaueste Näherung der aktuellen Beleuchtungsbedingungen zu erzielen, können Sie Daten von mehreren Umgebungslichtsensoren verwenden. Da Umgebungslichtsensoren teilweise oder vollständig durch Schatten oder Objekte verdeckt werden können, die den Sensor abdecken, können mehrere Sensoren, die etwas voneinander entfernt platziert werden, eine wesentlich bessere Annäherung an die aktuellen Beleuchtungsbedingungen bieten als ein einzelner Sensor.

Um die Daten von mehreren Sensoren nachzuverfolgen, können Sie die folgenden beiden Verfahren verwenden:

-   Der neueste Datenwert für jeden Umgebungslichtsensor kann zusammen mit dem Zeitstempel aus dem Sensordatenbericht für jeden dieser Messwerte beibehalten werden. Der letzte [**ISensorDataReport,**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) der für jeden Sensormesswert empfangen wurde, kann beibehalten werden und beide Werte für die spätere Referenz bereitstellen. Durch Verweisen auf den Zeitstempel für jeden Sensordatenbericht können die Daten basierend auf ihrem Alter verwaltet werden. Wenn die Daten beispielsweise mehr als 2 Sekunden alt sind, können sie ausgelassen werden. Basierend auf den neueren Sensordatenwerten kann der höchste Messwert verwendet werden, da davon ausgegangen wird, dass der entsprechende Sensor nicht verdeckt wird.
-   Sie können den letzten gemeldeten Umgebungslichtsensorwert verwenden. Diese Implementierung wäre nicht optimal, da die Werte mehrerer Sensoren nicht miteinander verglichen werden, um das genaueste Ergebnis zu erzielen. Diese Methode wird nicht empfohlen.

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode zeigt eine Implementierung für das [**OnDataUpdated-Ereignis.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) Der Ereignishandler ruft eine Hilfsfunktion namens **UpdateUI** auf, die die Benutzeroberfläche basierend auf dem Lux-Wert ändert. Es liegt an Ihnen, die Implementierung von UpdateUI zu schreiben.


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



 

 
