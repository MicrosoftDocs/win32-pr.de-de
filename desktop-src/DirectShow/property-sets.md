---
description: Eigenschaftensätze
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Eigenschaftensätze (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c26bef876e0bde559ac506963f86a485a302a9ce6faf6c2699c62dabac3f72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747950"
---
# <a name="property-sets-directshow"></a>Eigenschaftensätze (DirectShow)

Microsoft DirectShow verwendet Eigenschaftensätze, um erweiterte Dienste zu unterstützen, die von Hardware und den zugehörigen Treibern und Filtern angeboten werden. Hardware- und Filteranbieter können neue Funktionen als Eigenschaften definieren, sie in Eigenschaftensätzen anordnen und die Spezifikation für diese Eigenschaftensätze veröffentlichen. Als Anwendungsentwickler können Sie die Methoden der [**IKsPropertySet-Schnittstelle**](ikspropertyset.md) verwenden, um zu bestimmen, ob ein Treiber oder Filter einen bestimmten Satz von Eigenschaften unterstützt, und diese Eigenschaften abrufen oder festlegen.

Alle von **IKsPropertySet** verfügbar gemachten Methoden erfordern eine **GUID,** die den Eigenschaftensatz identifiziert (den *guidPropSet-Parameter)* und ein **DWORD,** das die Eigenschaft innerhalb des Eigenschaftensatzes identifiziert (dwPropID-Parameter).  Der *dwPropID-Parameter* ist in der Regel ein Member eines enumerationsierten Datentyps.

Einzelnen Eigenschaften können Daten zugeordnet sein, die Sie im *pPropData-Parameter* in den Methoden [**IKsPropertySet::Set**](ikspropertyset-set.md) und [**IKsPropertySet::Get**](ikspropertyset-get.md) angeben. In diesen Methoden werden die Eigenschaftsdaten als Zeiger auf `void` typisiert. Der Datentyp und die Bedeutung der Daten werden in der Definition des Eigenschaftensatzes angegeben.

Die folgenden Abschnitte enthalten Informationen zu den in DirectShow unterstützten Eigenschaftensätzen:

-   [**DVD Copy Protection-Eigenschaftensatz**](dvd-copy-protection-property-set.md)
-   [**DVD-Eigenschaftssatz "Dvd- UndOke"**](dvd-karaoke-property-set.md)
-   [**DVD Subpicture-Eigenschaftensatz**](dvd-subpicture-property-set.md)
-   [Eigenschaftensatz für den Transport externer Geräte](external-device-transport-property-set.md)
-   [Frame Stepping-Eigenschaftensatz](frame-stepping-property-set.md)
-   [Pin-Eigenschaftensatz](pin-property-set.md)
-   [**Ratenänderungseigenschaftensatz**](rate-change-property-set.md)

 

 



