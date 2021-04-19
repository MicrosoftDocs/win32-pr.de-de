---
description: Gibt den Typ des e/a-Busses an, der vom Grafikadapter verwendet wird.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: D3DBUSTYPE-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344232"
---
# <a name="d3dbustype-enumeration"></a><span data-ttu-id="29049-103">D3DBUSTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="29049-103">D3DBUSTYPE enumeration</span></span>

<span data-ttu-id="29049-104">Gibt den Typ des e/a-Busses an, der vom Grafikadapter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29049-104">Specifies the type of I/O bus used by the graphics adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="29049-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29049-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a><span data-ttu-id="29049-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="29049-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="29049-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ andere**</span><span class="sxs-lookup"><span data-stu-id="29049-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE\_OTHER**</span></span>
</dt> <dd>

<span data-ttu-id="29049-108">Gibt einen Typ von einem anderen Bus als den hier aufgeführten Typen an.</span><span class="sxs-lookup"><span data-stu-id="29049-108">Indicates a type of bus other than the types listed here.</span></span>

</dd> <dt>

<span data-ttu-id="29049-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="29049-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE\_PCI**</span></span>
</dt> <dd>

<span data-ttu-id="29049-110">PCI-Bus.</span><span class="sxs-lookup"><span data-stu-id="29049-110">PCI bus.</span></span>

</dd> <dt>

<span data-ttu-id="29049-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIx**</span><span class="sxs-lookup"><span data-stu-id="29049-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE\_PCIX**</span></span>
</dt> <dd>

<span data-ttu-id="29049-112">PCI-X-Bus.</span><span class="sxs-lookup"><span data-stu-id="29049-112">PCI-X bus.</span></span>

</dd> <dt>

<span data-ttu-id="29049-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIExpress**</span><span class="sxs-lookup"><span data-stu-id="29049-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE\_PCIEXPRESS**</span></span>
</dt> <dd>

<span data-ttu-id="29049-114">PCI-Express-Bus.</span><span class="sxs-lookup"><span data-stu-id="29049-114">PCI Express bus.</span></span>

</dd> <dt>

<span data-ttu-id="29049-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE- \_ AGP**</span><span class="sxs-lookup"><span data-stu-id="29049-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE\_AGP**</span></span>
</dt> <dd>

<span data-ttu-id="29049-116">AGP-Bus (Accelerated Graphics Port).</span><span class="sxs-lookup"><span data-stu-id="29049-116">Accelerated Graphics Port (AGP) bus.</span></span>

</dd> <dt>

<span data-ttu-id="29049-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL- \_ Modifizierer \_ innerhalb \_ des \_ Chipsets**</span><span class="sxs-lookup"><span data-stu-id="29049-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL\_MODIFIER\_INSIDE\_OF\_CHIPSET**</span></span>
</dt> <dd>

<span data-ttu-id="29049-118">Die Implementierung für den Grafikadapter befindet sich in der North Bridge eines Motherboard-Chipsatzes.</span><span class="sxs-lookup"><span data-stu-id="29049-118">The implementation for the graphics adapter is in a motherboard chipset's north bridge.</span></span> <span data-ttu-id="29049-119">Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. b. PCI oder AGP) übertragen werden, wenn Sie vom Hauptspeicher zum Grafikadapter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="29049-119">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="29049-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL- \_ \_ modifizierertitel \_ auf der \_ Mutter \_ Platine \_ in den \_ Chip**</span><span class="sxs-lookup"><span data-stu-id="29049-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_CHIP**</span></span>
</dt> <dd>

<span data-ttu-id="29049-121">Gibt an, dass der Grafikadapter mithilfe der Nachverfolgung auf der Hauptplatine mit der Nordbrücke eines Motherboard-Chipsatzes verbunden ist und alle Chips des Grafikadapters an die Platine soltet werden.</span><span class="sxs-lookup"><span data-stu-id="29049-121">Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard and all of the graphics adapter's chips are soldered to the motherboard.</span></span> <span data-ttu-id="29049-122">Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. b. PCI oder AGP) übertragen werden, wenn Sie vom Hauptspeicher zum Grafikadapter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="29049-122">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="29049-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL- \_ \_ modifizierertitel \_ auf \_ \_ dem Mutter Board \_ in \_ Socket**</span><span class="sxs-lookup"><span data-stu-id="29049-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_SOCKET**</span></span>
</dt> <dd>

<span data-ttu-id="29049-124">Der Grafikadapter ist mit der Nordbrücke eines Motherboard-Chipsatzes durch Nachverfolgung auf der Hauptplatine verbunden, und alle Chips des Grafikadapters sind über Sockets mit dem Motherboard verbunden.</span><span class="sxs-lookup"><span data-stu-id="29049-124">The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.</span></span>

</dd> <dt>

<span data-ttu-id="29049-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL- \_ modifiziererboard- \_ \_ \_ Connector**</span><span class="sxs-lookup"><span data-stu-id="29049-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="29049-126">Der Grafikadapter ist über einen Daughterboard-Connector mit dem Motherboard verbunden.</span><span class="sxs-lookup"><span data-stu-id="29049-126">The graphics adapter is connected to the motherboard through a daughterboard connector.</span></span>

</dd> <dt>

<span data-ttu-id="29049-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL- \_ modifiziererboard- \_ \_ \_ Connector \_ innerhalb \_ von \_ nuae**</span><span class="sxs-lookup"><span data-stu-id="29049-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR\_INSIDE\_OF\_NUAE**</span></span>
</dt> <dd>

<span data-ttu-id="29049-128">Der Grafikadapter ist über einen Daughterboard-Connector mit dem Motherboard verbunden, und der Grafikadapter befindet sich in einem Gehäuse, das nicht vom Benutzer zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="29049-128">The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.</span></span>

</dd> <dt>

<span data-ttu-id="29049-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL- \_ Modifizierer \_ nicht \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="29049-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL\_MODIFIER\_NON\_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="29049-130">Einer der D3DBUSIMPL-Modifizierer \_ \_ \_ xxx-Flags ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29049-130">One of the D3DBUSIMPL\_MODIFIER\_MODIFIER\_Xxx flags is set.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29049-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29049-131">Remarks</span></span>

<span data-ttu-id="29049-132">Es können bis zu drei Flags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="29049-132">As many as three flags can be set.</span></span> <span data-ttu-id="29049-133">Flags im Bereich von 0x00 bis 0x04 (**D3DBUSTYPE \_ xxx**) stellen den grundlegenden Bustyp bereit.</span><span class="sxs-lookup"><span data-stu-id="29049-133">Flags in the range 0x00 through 0x04 (**D3DBUSTYPE\_Xxx**) provide the basic bus type.</span></span> <span data-ttu-id="29049-134">Flags im Bereich von 0x10000 bis 0x50000 (**D3DBUSIMPL \_ Modifier \_ xxx**) ändern die grundlegende Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="29049-134">Flags in the range 0x10000 through 0x50000 (**D3DBUSIMPL\_MODIFIER\_Xxx**) modify the basic description.</span></span> <span data-ttu-id="29049-135">Der Treiber legt ein Flag für einen Bustyp fest und kann NULL oder ein modifiziererflag festlegen.</span><span class="sxs-lookup"><span data-stu-id="29049-135">The driver sets one bus-type flag, and can set zero or one modifier flag.</span></span> <span data-ttu-id="29049-136">Wenn der Treiber ein modifiziererflag festlegt, wird auch das Flag " **D3DBUSIMPL \_ Modifizierer \_ Non \_ Standard** " festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29049-136">If the driver sets a modifier flag, it also sets the **D3DBUSIMPL\_MODIFIER\_NON\_STANDARD** flag.</span></span> <span data-ttu-id="29049-137">Flags werden mit einem bitweisen **or** kombiniert.</span><span class="sxs-lookup"><span data-stu-id="29049-137">Flags are combined with a bitwise **OR**.</span></span>

## <a name="requirements"></a><span data-ttu-id="29049-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29049-138">Requirements</span></span>



| <span data-ttu-id="29049-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29049-139">Requirement</span></span> | <span data-ttu-id="29049-140">Wert</span><span class="sxs-lookup"><span data-stu-id="29049-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29049-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29049-141">Minimum supported client</span></span><br/> | <span data-ttu-id="29049-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29049-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="29049-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29049-143">Minimum supported server</span></span><br/> | <span data-ttu-id="29049-144">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29049-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="29049-145">Header</span><span class="sxs-lookup"><span data-stu-id="29049-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="29049-146"><dt>D3d9types. h (Include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29049-146"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29049-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29049-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29049-148">Direct3D-videoenumerationen</span><span class="sxs-lookup"><span data-stu-id="29049-148">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




