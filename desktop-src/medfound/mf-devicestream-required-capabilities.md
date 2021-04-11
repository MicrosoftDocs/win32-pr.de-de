---
description: Gibt eine Liste von Unicode-Zeichen folgen an, die die von der Sensor Transformation benötigten Gerätefunktionen darstellen.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: MF_DEVICESTREAM_REQUIRED_CAPABILITIES-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129789"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a><span data-ttu-id="bc377-103">Erforderliche Funktionen für das MF- \_ devicestream- \_ \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="bc377-103">MF\_DEVICESTREAM\_REQUIRED\_CAPABILITIES attribute</span></span>

<span data-ttu-id="bc377-104">Gibt eine Liste von Unicode-Zeichen folgen an, die die von der Sensor Transformation benötigten Gerätefunktionen darstellen.</span><span class="sxs-lookup"><span data-stu-id="bc377-104">Specifies a list of unicode strings representing the device capabilities required by the sensor transform.</span></span>

## <a name="data-type"></a><span data-ttu-id="bc377-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bc377-105">Data type</span></span>

<span data-ttu-id="bc377-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="bc377-106">\**WCHAR\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="bc377-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc377-107">Remarks</span></span>

<span data-ttu-id="bc377-108">Dieses Attribut ist optional und nur erforderlich, wenn die Sensor Transformation auf eine geschützte Ressource zugreift.</span><span class="sxs-lookup"><span data-stu-id="bc377-108">This attribute is optional and only required if the sensor transform accesses a protected resource.</span></span> <span data-ttu-id="bc377-109">Der Wert muss eine durch Semikolons getrennte Liste von Zeichen folgen Token sein, die in [_ "*endvicecapability* \*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability)" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bc377-109">The value must be a semicolon delimited list of string tokens defined in [_ *DeviceCapability*\*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc377-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc377-110">Requirements</span></span>



| <span data-ttu-id="bc377-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc377-111">Requirement</span></span> | <span data-ttu-id="bc377-112">Wert</span><span class="sxs-lookup"><span data-stu-id="bc377-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc377-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc377-113">Minimum supported client</span></span><br/> | <span data-ttu-id="bc377-114">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc377-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bc377-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc377-115">Minimum supported server</span></span><br/> | <span data-ttu-id="bc377-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc377-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="bc377-117">Header</span><span class="sxs-lookup"><span data-stu-id="bc377-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc377-118"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc377-118"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
