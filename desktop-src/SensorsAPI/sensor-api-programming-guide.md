---
description: Dieser Abschnitt enthält Informationen einschließlich Beispielcode zur Verwendung der Sensor-API-Funktionen. Hintergrundinformationen zu den verschiedenen Programmierschnittstellen finden Sie unter Informationen zur Sensor-API.
ms.assetid: 4c2ffd22-49ee-4318-bfa0-e0ce4d8c67bb
title: Programmier Handbuch zur Sensor-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078cc99e88a1a4fd6a232220e08c53a99dfbdfb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347132"
---
# <a name="sensor-api-programming-guide"></a>Programmier Handbuch zur Sensor-API

Dieser Abschnitt enthält Informationen einschließlich Beispielcode zur Verwendung der Sensor-API-Funktionen. Hintergrundinformationen zu den verschiedenen Programmierschnittstellen finden Sie unter Informationen zur [Sensor-API](about-the-sensor-api.md).

Der Beispielcode in diesem Abschnitt verwendet die folgenden zusätzlichen enthaltenen Header.


```C++
#include <windows.h>
#include <initguid.h>
#include <propkeydef.h>


#include <iostream>
#include <propvarutil.h>
#include <functiondiscoverykeys.h>
#include <assert.h>
```





Sie müssen auch eine Verknüpfung zu diesen zusätzlichen zugeordneten Bibliotheksdateien herstellen: "propsys. lib" und "portabledeviceguids. lib".

Der Beispielcode in diesem Abschnitt verwendet die folgenden Konstanten für Sensor Kategorien, Typen und Datenfelder. Diese Konstanten sind benutzerdefinierte Werte, die durch das Beispiel für einen timesensor-Treiber im Windows-Treiberkit definiert werden. Beachten Sie Folgendes: Obwohl die Sensor Plattform das definieren und Verwenden von benutzerdefinierten Typen wie diesen ermöglicht, sollten Sie nach Möglichkeit Platt Form definierte Typen verwenden.


```C++
// Define an object ID.
// {0D77BEE3-7169-42bf-8379-28F9A9B59A57}
DEFINE_GUID(SAMPLE_SENSOR_TIME_ID, 
0xd77bee3, 0x7169, 0x42bf, 0x83, 0x79, 0x28, 0xf9, 0xa9, 0xb5, 0x9a, 0x57);

// Define a custom category.
// {062A5C3B-44C1-4ad1-8EFC-0F65B2E4AD48}
DEFINE_GUID(SAMPLE_SENSOR_CATEGORY_DATE_TIME, 
0x62a5c3b, 0x44c1, 0x4ad1, 0x8e, 0xfc, 0xf, 0x65, 0xb2, 0xe4, 0xad, 0x48);

// Define a custom type.
// {5F199A84-409F-4e35-B2DD-F9C79F5318A0}
DEFINE_GUID(SAMPLE_SENSOR_TYPE_TIME, 
0x5f199a84, 0x409f, 0x4e35, 0xb2, 0xdd, 0xf9, 0xc7, 0x9f, 0x53, 0x18, 0xa0);

// Time sensor fields.
// Because these are related, each field uses the same GUID, but changes the PID.
// {340946F2-9A77-42b0-8176-57D4DF00E5CA}
DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_HOUR, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE); // PID = 2

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_MINUTE, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 1); // PID = 3

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_SECOND, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 2); // PID = 4
```



Der Beispielcode in diesem Abschnitt verwendet die folgenden Variablen.


```C++
HRESULT hr = S_OK;

// Sensor interface pointers
ISensorManager* pSensorManager = NULL;    
ISensorCollection* pSensorColl = NULL;
ISensor* pSensor = NULL; 
ISensorDataReport* pReport = NULL;

// Time sensor data field variables
ULONG ulHour, ulMinute, ulSecond = 0;

```



Der Beispielcode in diesem Abschnitt verwendet die folgende Funktion, um COM-Schnittstellen Zeiger freizugeben.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="in-this-section"></a>In diesem Abschnitt

-   [Abrufen eines Sensor Objekts](retrieving-a-sensor.md)
-   [Anfordern von Benutzerberechtigungen](requesting-user-permissions.md)
-   [Abrufen und Festlegen von Sensor Eigenschaften](setting-and-retrieving-sensor-properties.md)
-   [Überprüfen auf unterstützte Sensor Datenfelder](checking-for-supported-sensor-data-fields.md)
-   [Verwenden von Sensor-API-Ereignissen](using-sensor-api-events.md)
-   [Abrufen von Sensor Datenwerten](retrieving-sensor-data-fields.md)
-   [Abrufen von Vektor Typen](retrieving-vector-types.md)
-   [Verwenden logischer Sensoren](using-logical-sensors.md)
-   [Erstellen Light-Aware Benutzeroberflächen](creating-light-aware-user-interfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Sensor-API](about-the-sensor-api.md)
</dt> </dl>

 

 



