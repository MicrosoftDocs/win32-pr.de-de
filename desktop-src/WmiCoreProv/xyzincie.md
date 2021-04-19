---
description: Enthält die Koordinaten der Anzeige im Bereich der International Commission on Illumination (CIE) XYZ-Farbraum.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Xyzincie-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356988"
---
# <a name="xyzincie-class"></a><span data-ttu-id="47c69-103">Xyzincie-Klasse</span><span class="sxs-lookup"><span data-stu-id="47c69-103">XYZinCIE class</span></span>

<span data-ttu-id="47c69-104">Die **xyzincie** WMI-Klasse enthält die Koordinaten der Anzeige im Bereich der International Commission on Illumination (CIE) XYZ-Farbraum.</span><span class="sxs-lookup"><span data-stu-id="47c69-104">The **XYZinCIE** WMI class contains the coordinates of the display in the International Commission on Illumination (CIE) XYZ color space.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47c69-105">Syntax</span></span>

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a><span data-ttu-id="47c69-106">Member</span><span class="sxs-lookup"><span data-stu-id="47c69-106">Members</span></span>

<span data-ttu-id="47c69-107">Die **xyzincie** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47c69-107">The **XYZinCIE** class has these types of members:</span></span>

-   [<span data-ttu-id="47c69-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47c69-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47c69-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47c69-109">Properties</span></span>

<span data-ttu-id="47c69-110">Die **xyzincie** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47c69-110">The **XYZinCIE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47c69-111">**X**</span><span class="sxs-lookup"><span data-stu-id="47c69-111">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c69-112">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="47c69-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="47c69-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47c69-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47c69-114">X-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="47c69-114">X-coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="47c69-115">**J**</span><span class="sxs-lookup"><span data-stu-id="47c69-115">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c69-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="47c69-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="47c69-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="47c69-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47c69-118">Y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="47c69-118">Y-coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47c69-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47c69-119">Remarks</span></span>

<span data-ttu-id="47c69-120">Die [**wmimonitorcolorcharacteristics**](wmimonitorcolorcharacteristics.md) -Klasse enthält eingebettete Instanzen der **xyzincie** -Klasse, um die Farbmerkmale eines Monitors zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="47c69-120">The [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) class contains embedded instances of the **XYZinCIE** class to describe the color characteristics of a monitor.</span></span>

<span data-ttu-id="47c69-121">Um die z-Koordinate basierend auf den x-und y-Werten zu berechnen, verwenden Sie die-Beziehung \| \| (x, y, z) \| \| = 1.</span><span class="sxs-lookup"><span data-stu-id="47c69-121">To calculate the z-coordinate, based on the x and y values, use the relation \|\|(x,y,z)\|\| = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c69-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47c69-122">Requirements</span></span>



| <span data-ttu-id="47c69-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47c69-123">Requirement</span></span> | <span data-ttu-id="47c69-124">Wert</span><span class="sxs-lookup"><span data-stu-id="47c69-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47c69-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47c69-125">Minimum supported client</span></span><br/> | <span data-ttu-id="47c69-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47c69-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="47c69-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47c69-127">Minimum supported server</span></span><br/> | <span data-ttu-id="47c69-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47c69-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="47c69-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="47c69-129">Namespace</span></span><br/>                | <span data-ttu-id="47c69-130">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="47c69-130">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="47c69-131">MOF</span><span class="sxs-lookup"><span data-stu-id="47c69-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47c69-132"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="47c69-132"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="47c69-133">DLL</span><span class="sxs-lookup"><span data-stu-id="47c69-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c69-134"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47c69-134"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c69-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47c69-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c69-136">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="47c69-136">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




