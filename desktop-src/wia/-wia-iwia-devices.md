---
description: Sammlung von DeviceInfo-Objekten, die alle auf dem Computer installierten Geräte darstellt.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Wia.Devices-Eigenschaft
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
ms.openlocfilehash: b4d98bfe1552156071efde0b46899ad058e75aec
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841312"
---
# <a name="wiadevices-property"></a><span data-ttu-id="fb546-103">Wia.Devices-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fb546-103">Wia.Devices property</span></span>

<span data-ttu-id="fb546-104">Sammlung von [**DeviceInfo-Objekten,**](-wia-deviceinfo.md) die alle auf dem Computer installierten Geräte darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb546-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="fb546-105">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fb546-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="fb546-106">Diese Auflistung ist 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="fb546-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="fb546-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fb546-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb546-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb546-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="fb546-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fb546-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="fb546-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb546-110">Examples</span></span>

<span data-ttu-id="fb546-111">Im folgenden Beispiel wird die Verwendung der Sammlung **Geräte** zum Aufzählen der Geräte auf einem System veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fb546-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fb546-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb546-112">Requirements</span></span>



| <span data-ttu-id="fb546-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb546-113">Requirement</span></span> | <span data-ttu-id="fb546-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fb546-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb546-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb546-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fb546-116">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb546-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb546-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb546-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fb546-118">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb546-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fb546-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fb546-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb546-120"><dt>Wiascr.dll (Version 4.90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fb546-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




