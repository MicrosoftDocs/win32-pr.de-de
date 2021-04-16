---
description: Einige Eigenschaften und Datenfelder enthalten Arrays von Informationen.
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: Abrufen von Vektor Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945b45e4e78b6c4f9f9e0fb4b3848f813549105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525652"
---
# <a name="retrieving-vector-types"></a>Abrufen von Vektor Typen

Einige Eigenschaften und Datenfelder enthalten Arrays von Informationen. Beispielsweise \_ \_ enthält die \_ Eigenschaft hell Response-Eigenschaft der Sensor Eigenschaft \_ ein Array von 4-Byte-Ganzzahlen ohne Vorzeichen. Wenn Sie jedoch solche Arrays über die Sensor-API erhalten, werden Sie immer als Typ VT \_ Vector \| UI1, ein Array von Einzel Byte Zeichen, unabhängig vom tatsächlichen Typ der Daten im Array dargestellt. Für diese Typen müssen Sie darauf achten, Array Variablen in den richtigen Datentyp für die Eigenschaft oder das Datenfeld umzuwandeln.

Informationen zu Eigenschaften, Datenfeldern und deren Typen finden Sie unter [Konstanten](constants.md).

Der folgende Beispielcode zeigt, wie die in der Sensor \_ Eigenschaft Light Response-Kurve abgerufenen Daten \_ \_ \_ in den richtigen Typ umgewandelt werden.


```C++
PROPVARIANT pvCurve;
PropVariantInit(&pvCurve);

// Retrieve the property value.
hr = pSensor->GetProperty(SENSOR_PROPERTY_LIGHT_RESPONSE_CURVE, &pvCurve);
if (SUCCEEDED(hr))
{
    if ((VT_UI1|VT_VECTOR) == V_VT(pvCurve)) // Note actual type of UI1
    {
        // Cast the array to UINT, a 4-byte unsigned integer.

        // Item count for the array.
        UINT  cElement = pvCurve.caub.cElems/sizeof(UINT);
        // Array pointer.
        UINT* pElement = (UINT*)(pvCurve.caub.pElems);

        // Use the array.
    }
}

// Remember to free the PROPVARIANT when done.
PropVariantClear(&pvCurve);
```



 

 



