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
# <a name="retrieving-vector-types"></a><span data-ttu-id="b53a6-103">Abrufen von Vektor Typen</span><span class="sxs-lookup"><span data-stu-id="b53a6-103">Retrieving Vector Types</span></span>

<span data-ttu-id="b53a6-104">Einige Eigenschaften und Datenfelder enthalten Arrays von Informationen.</span><span class="sxs-lookup"><span data-stu-id="b53a6-104">Some properties and data fields contain arrays of information.</span></span> <span data-ttu-id="b53a6-105">Beispielsweise \_ \_ enthält die \_ Eigenschaft hell Response-Eigenschaft der Sensor Eigenschaft \_ ein Array von 4-Byte-Ganzzahlen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="b53a6-105">For example, the SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE property contains an array of 4-byte unsigned integers.</span></span> <span data-ttu-id="b53a6-106">Wenn Sie jedoch solche Arrays über die Sensor-API erhalten, werden Sie immer als Typ VT \_ Vector \| UI1, ein Array von Einzel Byte Zeichen, unabhängig vom tatsächlichen Typ der Daten im Array dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b53a6-106">However, when you receive such arrays through the Sensor API, they are always represented as type VT\_VECTOR\|UI1, an array of single-byte characters, regardless of the actual type of the data in the array.</span></span> <span data-ttu-id="b53a6-107">Für diese Typen müssen Sie darauf achten, Array Variablen in den richtigen Datentyp für die Eigenschaft oder das Datenfeld umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="b53a6-107">For these types, you must be careful to cast array variables to the correct data type for the property or data field.</span></span>

<span data-ttu-id="b53a6-108">Informationen zu Eigenschaften, Datenfeldern und deren Typen finden Sie unter [Konstanten](constants.md).</span><span class="sxs-lookup"><span data-stu-id="b53a6-108">For information about properties, data fields, and their types, see [Constants](constants.md).</span></span>

<span data-ttu-id="b53a6-109">Der folgende Beispielcode zeigt, wie die in der Sensor \_ Eigenschaft Light Response-Kurve abgerufenen Daten \_ \_ \_ in den richtigen Typ umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="b53a6-109">The following example code shows how to cast the data retrieved in SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE to the correct type.</span></span>


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



 

 



