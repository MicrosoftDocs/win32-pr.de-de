---
description: Jede Eigenschaft in einer Ansichts Klasse muss über einen Zeichen folgen Array-Qualifizierer namens propertysources verfügen.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Propertysources-Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357420"
---
# <a name="propertysources-qualifier"></a><span data-ttu-id="3efa4-103">Propertysources-Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="3efa4-103">PropertySources Qualifier</span></span>

<span data-ttu-id="3efa4-104">Jede Eigenschaft in einer Ansichts Klasse muss über einen Zeichen folgen Array-Qualifizierer namens **propertysources** verfügen.</span><span class="sxs-lookup"><span data-stu-id="3efa4-104">Every property in a view class must have a string array qualifier called **PropertySources**.</span></span> <span data-ttu-id="3efa4-105">Der **propertysources** -Qualifizierer enthält den Namen der Quell Klassen Eigenschaft oder der Eigenschaften, von denen diese Eigenschaft der Ansichts Klasse Daten abruft.</span><span class="sxs-lookup"><span data-stu-id="3efa4-105">The **PropertySources** qualifier contains the name of the source class property or properties from which this view class property gets data.</span></span> <span data-ttu-id="3efa4-106">Die Reihenfolge der Werte in diesem Array entspricht der Reihenfolge der Quell Klassen, die für den [viewsources-Qualifizierer](viewsources-qualifier.md)definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3efa4-106">The order of the values in this array correspond to the order of the source classes defined for the [ViewSources qualifier](viewsources-qualifier.md).</span></span> <span data-ttu-id="3efa4-107">Im folgenden Beispiel wird gezeigt, wie eine Eigenschaft für eine Union-Ansichts Klasse definiert wird, die die Union der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse von zwei verschiedenen Computern ist:</span><span class="sxs-lookup"><span data-stu-id="3efa4-107">The following example shows how to define a property for a union view class that is the union of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class from two different computers:</span></span>


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



<span data-ttu-id="3efa4-108">Die erste **DeviceID** -Eigenschaft entspricht der **DeviceID** -Eigenschaft aus der-Klasse in der ersten Quell Abfrage.</span><span class="sxs-lookup"><span data-stu-id="3efa4-108">The first **DeviceID** property corresponds to the **DeviceID** property from the class in the first source query.</span></span> <span data-ttu-id="3efa4-109">Die zweite Eigenschaft " **DeviceID** " ist die Eigenschaft " **DeviceID** " aus der-Klasse in der zweiten Quell Abfrage.</span><span class="sxs-lookup"><span data-stu-id="3efa4-109">The second **DeviceID** property is the **DeviceID** property from the class in the second source query.</span></span>

<span data-ttu-id="3efa4-110">Wenn Sie Eigenschaften für joinansichts Klassen definieren, müssen Sie eine separate Ansichts Eigenschaft für jede der Quell Klasseneigenschaften definieren, es sei denn, die Quell Klasseneigenschaften sind die Basis der joinansichts Klasse.</span><span class="sxs-lookup"><span data-stu-id="3efa4-110">When defining properties for join view classes, you must define a separate view property for each of the source class properties unless the source class properties are the basis of the join view class.</span></span> <span data-ttu-id="3efa4-111">Im folgenden Beispiel werden Eigenschaften in einer joinansichts Klasse für ähnliche Eigenschaften der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Quell Klasse und der [**Win32 \_ printerconfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) -Quell Klasse erstellt:</span><span class="sxs-lookup"><span data-stu-id="3efa4-111">The following example creates properties in a join view class on similar properties from the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) source class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) source class:</span></span>


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



<span data-ttu-id="3efa4-112">Wenn die beiden Quell Klassen durch eine gemeinsame Eigenschaft verknüpft werden, können Sie nur eine einzelne Ansichts Klassen Eigenschaft definieren, da der Wert beider Quell Klasseneigenschaften immer identisch ist.</span><span class="sxs-lookup"><span data-stu-id="3efa4-112">If the two source classes are being joined by a common property, you can only define a single view class property because the value of both source class properties is always the same.</span></span> <span data-ttu-id="3efa4-113">Im folgenden Beispiel wird gezeigt, wie die [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse und die [**Win32- \_ printerconfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) durch einen allgemeinen Eigenschafts Wert verknüpft werden:</span><span class="sxs-lookup"><span data-stu-id="3efa4-113">The following example shows how to join the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) by a common property value:</span></span>


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a><span data-ttu-id="3efa4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3efa4-114">Requirements</span></span>



| <span data-ttu-id="3efa4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3efa4-115">Requirement</span></span> | <span data-ttu-id="3efa4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3efa4-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3efa4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3efa4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3efa4-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3efa4-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3efa4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3efa4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3efa4-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3efa4-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3efa4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3efa4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3efa4-122">**Spezifische Qualifizierer für den Ansichts Anbieter**</span><span class="sxs-lookup"><span data-stu-id="3efa4-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

