---
description: Stellt Eingabeparameter für digitales Video dar.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Wmimonitordigitalvideoinputparameams-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366071"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a><span data-ttu-id="1ee73-103">Wmimonitordigitalvideoinputparameams-Klasse</span><span class="sxs-lookup"><span data-stu-id="1ee73-103">WmiMonitorDigitalVideoInputParams class</span></span>

<span data-ttu-id="1ee73-104">**Wmimonitordigitalvideoinputparameams** stellt Eingabeparameter für digitales Video dar.</span><span class="sxs-lookup"><span data-stu-id="1ee73-104">The **WmiMonitorDigitalVideoInputParams** represents input parameters for digital video.</span></span> <span data-ttu-id="1ee73-105">Die Daten in dieser Klasse entsprechen den Daten in der Videoeingabe Definition von "velectronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) Standard".</span><span class="sxs-lookup"><span data-stu-id="1ee73-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="1ee73-106">Eine Instanz dieser Klasse ist nur verfügbar, wenn der Wert der **videoinputtype** -Eigenschaft der [**wmimonitorbasicdisplaypara**](wmimonitorbasicdisplayparams.md) -Klasse "Digital" ist.</span><span class="sxs-lookup"><span data-stu-id="1ee73-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Digital".</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee73-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ee73-107">Syntax</span></span>

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a><span data-ttu-id="1ee73-108">Member</span><span class="sxs-lookup"><span data-stu-id="1ee73-108">Members</span></span>

<span data-ttu-id="1ee73-109">Die **wmimonitordigitalvideoinputparameams** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1ee73-109">The **WmiMonitorDigitalVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="1ee73-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ee73-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ee73-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ee73-111">Properties</span></span>

<span data-ttu-id="1ee73-112">Die **wmimonitordigitalvideoinputparser** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ee73-112">The **WmiMonitorDigitalVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ee73-113">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="1ee73-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee73-114">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1ee73-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ee73-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ee73-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ee73-116">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="1ee73-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="1ee73-117">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1ee73-117">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee73-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ee73-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ee73-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ee73-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ee73-120">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1ee73-120">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1ee73-121">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="1ee73-121">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="1ee73-122">**IsDFP1xCompatible**</span><span class="sxs-lookup"><span data-stu-id="1ee73-122">**IsDFP1xCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee73-123">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1ee73-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ee73-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ee73-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ee73-125">VESA DFP 1. x oder kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1ee73-125">VESA DFP 1.x or compatible.</span></span> <span data-ttu-id="1ee73-126">Wenn diese Option festgelegt ist, ist die Schnittstelle Signal kompatibel mit VESA Digital Flat Panel (DFP) 1. x Übergang minimids (Minimum Differential signds) crgb, 1 Pixel/Clock, bis zu 8 Bits/Farbe, das am signifikantesten (am wichtigsten ist), de aktiv hoch.</span><span class="sxs-lookup"><span data-stu-id="1ee73-126">If set, interface is signal compatible with VESA Digital Flat Panel (DFP) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 pixel/clock, up to 8 bits/color most significant bit (MSB) aligned, DE active high.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ee73-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ee73-127">Requirements</span></span>



| <span data-ttu-id="1ee73-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ee73-128">Requirement</span></span> | <span data-ttu-id="1ee73-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1ee73-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee73-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ee73-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee73-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ee73-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1ee73-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ee73-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee73-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ee73-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1ee73-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ee73-134">Namespace</span></span><br/>                | <span data-ttu-id="1ee73-135">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="1ee73-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1ee73-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1ee73-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ee73-137"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1ee73-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ee73-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1ee73-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ee73-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ee73-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee73-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ee73-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee73-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1ee73-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




