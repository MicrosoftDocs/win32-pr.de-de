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
# <a name="property-sets-directshow"></a><span data-ttu-id="e51b8-103">Eigenschaften Sätze (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e51b8-103">Property Sets (DirectShow)</span></span>

<span data-ttu-id="e51b8-104">Microsoft DirectShow verwendet Eigenschafts Gruppen zur Unterstützung erweiterter Dienste, die von der Hardware und den zugehörigen Treibern und Filtern angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="e51b8-104">Microsoft DirectShow uses property sets to support extended services offered by hardware and its associated drivers and filters.</span></span> <span data-ttu-id="e51b8-105">Hardware-und Filter Anbieter können neue Funktionen als Eigenschaften definieren, Sie in Eigenschafts Sätzen anordnen und die Spezifikation für diese Eigenschaften Sätze veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="e51b8-105">Hardware and filter vendors can define new capabilities as properties, arrange them in property sets, and publish the specification for these property sets.</span></span> <span data-ttu-id="e51b8-106">Als Anwendungsentwickler können Sie die Methoden der " [**ikspropertyset**](ikspropertyset.md) "-Schnittstelle verwenden, um zu bestimmen, ob ein Treiber oder Filter eine bestimmte Gruppe von Eigenschaften unterstützt, und diese Eigenschaften abrufen oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="e51b8-106">As the application developer, you can use the methods of the [**IKsPropertySet**](ikspropertyset.md) interface to determine whether a driver or filter supports a particular set of properties, and retrieve or set those properties.</span></span>

<span data-ttu-id="e51b8-107">Alle Methoden, die von " **ikspropertyset** " verfügbar gemacht werden, erfordern eine **GUID** , die den Eigenschaften Satz (den *guidpropset* -Parameter) und ein **DWORD** identifiziert, das die Eigenschaft innerhalb des Eigenschaften Satzes (dem *dwpropid* -Parameter) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e51b8-107">All the methods exposed by **IKsPropertySet** require a **GUID** that identifies the property set (the *guidPropSet* parameter) and a **DWORD** that identifies the property within the property set (the *dwPropID* parameter).</span></span> <span data-ttu-id="e51b8-108">Der *dwpropid* -Parameter ist in der Regel ein Member eines enumerierten Datentyps.</span><span class="sxs-lookup"><span data-stu-id="e51b8-108">The *dwPropID* parameter is typically a member of an enumerated data type.</span></span>

<span data-ttu-id="e51b8-109">Einzelnen Eigenschaften können zugeordnete Daten zugeordnet werden, die Sie im Parameter " *ppropdata* " in den Methoden " [**ikspropertyset:: set**](ikspropertyset-set.md) " und " [**ikspropertyset:: Get**](ikspropertyset-get.md) " angeben.</span><span class="sxs-lookup"><span data-stu-id="e51b8-109">Individual properties can have associated data that you specify in the *pPropData* parameter in the [**IKsPropertySet::Set**](ikspropertyset-set.md) and [**IKsPropertySet::Get**](ikspropertyset-get.md) methods.</span></span> <span data-ttu-id="e51b8-110">In diesen Methoden werden die Eigenschaften Daten als Zeiger auf typisiert `void` .</span><span class="sxs-lookup"><span data-stu-id="e51b8-110">In these methods, the property data is typed as a pointer to `void`.</span></span> <span data-ttu-id="e51b8-111">Der-Datentyp und die Bedeutung der Daten werden in der Definition des Eigenschaften Satzes angegeben.</span><span class="sxs-lookup"><span data-stu-id="e51b8-111">The data type and the meaning of the data are specified in the definition of the property set.</span></span>

<span data-ttu-id="e51b8-112">Die folgenden Abschnitte enthalten Informationen zu den in DirectShow unterstützten Eigenschaften Sätzen:</span><span class="sxs-lookup"><span data-stu-id="e51b8-112">The following sections provide information about the property sets supported in DirectShow:</span></span>

-   [<span data-ttu-id="e51b8-113">**Eigenschaften Satz für den DVD-Kopierschutz**</span><span class="sxs-lookup"><span data-stu-id="e51b8-113">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="e51b8-114">**DVD-Karaoke-Eigenschaften Satz**</span><span class="sxs-lookup"><span data-stu-id="e51b8-114">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="e51b8-115">**Eigenschaften Satz des DVD-Teil Bilds**</span><span class="sxs-lookup"><span data-stu-id="e51b8-115">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="e51b8-116">Eigenschaften Satz für externen Geräte Transport</span><span class="sxs-lookup"><span data-stu-id="e51b8-116">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
-   [<span data-ttu-id="e51b8-117">Frame Step-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="e51b8-117">Frame Stepping Property Set</span></span>](frame-stepping-property-set.md)
-   [<span data-ttu-id="e51b8-118">PIN-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="e51b8-118">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="e51b8-119">**Eigenschaften Satz für Raten Änderung**</span><span class="sxs-lookup"><span data-stu-id="e51b8-119">**Rate Change Property Set**</span></span>](rate-change-property-set.md)

 

 



