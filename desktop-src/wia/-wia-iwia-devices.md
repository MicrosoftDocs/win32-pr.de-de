---
description: Sammlung von "de viceinfo"-Objekten, die alle auf dem Computer installierten Geräte darstellen.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: WIA. Devices (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d03aa0b7e73d5dfbc6449816f3b64147e51db882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356533"
---
# <a name="wiadevices-property"></a><span data-ttu-id="dadbe-103">WIA. Devices (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dadbe-103">Wia.Devices property</span></span>

<span data-ttu-id="dadbe-104">Sammlung von " [**de viceinfo**](-wia-deviceinfo.md) "-Objekten, die alle auf dem Computer installierten Geräte darstellen.</span><span class="sxs-lookup"><span data-stu-id="dadbe-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="dadbe-105">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dadbe-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="dadbe-106">Diese Auflistung ist 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="dadbe-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="dadbe-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dadbe-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dadbe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dadbe-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="dadbe-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dadbe-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="dadbe-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dadbe-110">Examples</span></span>

<span data-ttu-id="dadbe-111">Das folgende Beispiel veranschaulicht die Verwendung der **Geräte** Auflistung zum Auflisten der Geräte in einem System.</span><span class="sxs-lookup"><span data-stu-id="dadbe-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="dadbe-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dadbe-112">Requirements</span></span>



| <span data-ttu-id="dadbe-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dadbe-113">Requirement</span></span> | <span data-ttu-id="dadbe-114">Wert</span><span class="sxs-lookup"><span data-stu-id="dadbe-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dadbe-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dadbe-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dadbe-116">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dadbe-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dadbe-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dadbe-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dadbe-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dadbe-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dadbe-119">DLL</span><span class="sxs-lookup"><span data-stu-id="dadbe-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dadbe-120"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="dadbe-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




