---
description: Eigenschaftensätze
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Eigenschaften Sätze (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392561"
---
# <a name="property-sets-directshow"></a>Eigenschaften Sätze (DirectShow)

Microsoft DirectShow verwendet Eigenschafts Gruppen zur Unterstützung erweiterter Dienste, die von der Hardware und den zugehörigen Treibern und Filtern angeboten werden. Hardware-und Filter Anbieter können neue Funktionen als Eigenschaften definieren, Sie in Eigenschafts Sätzen anordnen und die Spezifikation für diese Eigenschaften Sätze veröffentlichen. Als Anwendungsentwickler können Sie die Methoden der " [**ikspropertyset**](ikspropertyset.md) "-Schnittstelle verwenden, um zu bestimmen, ob ein Treiber oder Filter eine bestimmte Gruppe von Eigenschaften unterstützt, und diese Eigenschaften abrufen oder festlegen.

Alle Methoden, die von " **ikspropertyset** " verfügbar gemacht werden, erfordern eine **GUID** , die den Eigenschaften Satz (den *guidpropset* -Parameter) und ein **DWORD** identifiziert, das die Eigenschaft innerhalb des Eigenschaften Satzes (dem *dwpropid* -Parameter) identifiziert. Der *dwpropid* -Parameter ist in der Regel ein Member eines enumerierten Datentyps.

Einzelnen Eigenschaften können zugeordnete Daten zugeordnet werden, die Sie im Parameter " *ppropdata* " in den Methoden " [**ikspropertyset:: set**](ikspropertyset-set.md) " und " [**ikspropertyset:: Get**](ikspropertyset-get.md) " angeben. In diesen Methoden werden die Eigenschaften Daten als Zeiger auf typisiert `void` . Der-Datentyp und die Bedeutung der Daten werden in der Definition des Eigenschaften Satzes angegeben.

Die folgenden Abschnitte enthalten Informationen zu den in DirectShow unterstützten Eigenschaften Sätzen:

-   [**Eigenschaften Satz für den DVD-Kopierschutz**](dvd-copy-protection-property-set.md)
-   [**DVD-Karaoke-Eigenschaften Satz**](dvd-karaoke-property-set.md)
-   [**Eigenschaften Satz des DVD-Teil Bilds**](dvd-subpicture-property-set.md)
-   [Eigenschaften Satz für externen Geräte Transport](external-device-transport-property-set.md)
-   [Frame Step-Eigenschaften Satz](frame-stepping-property-set.md)
-   [PIN-Eigenschaften Satz](pin-property-set.md)
-   [**Eigenschaften Satz für Raten Änderung**](rate-change-property-set.md)

 

 



