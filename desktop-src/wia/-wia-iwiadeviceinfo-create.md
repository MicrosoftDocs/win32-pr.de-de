---
description: Die Create-Methode des DeviceInfo-Objekts stellt eine Verbindung mit dem durch das deviceInfo-Objekt angegebenen Windows-Abbild Erfassungsgerät (WIA) her und gibt ein Element Objekt zurück, das das Gerät darstellt.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: Deviceingefo. Create-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372881"
---
# <a name="deviceinfocreate-method"></a><span data-ttu-id="c91ab-103">Deviceingefo. Create-Methode</span><span class="sxs-lookup"><span data-stu-id="c91ab-103">DeviceInfo.Create method</span></span>

<span data-ttu-id="c91ab-104">Die **Create** -Methode des [**deviceInfo**](-wia-deviceinfo.md) -Objekts stellt eine Verbindung mit dem durch das **deviceInfo** -Objekt angegebenen Windows-Abbild Erfassungsgerät (WIA) her und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="c91ab-104">The **Create** method of the [**DeviceInfo**](-wia-deviceinfo.md) object makes a connection to the Windows Image Acquisition (WIA) device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c91ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c91ab-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a><span data-ttu-id="c91ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c91ab-106">Parameters</span></span>

<span data-ttu-id="c91ab-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c91ab-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c91ab-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c91ab-108">Return value</span></span>

<span data-ttu-id="c91ab-109">Typ: **iwiadispatchitem**</span><span class="sxs-lookup"><span data-stu-id="c91ab-109">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="c91ab-110">Diese Methode gibt das [**Item**](-wia-item.md) -Objekt zurück, das das erstellte Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="c91ab-110">This method returns the [**Item**](-wia-item.md) object that represents the device that is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="c91ab-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c91ab-111">Remarks</span></span>

<span data-ttu-id="c91ab-112">Verwenden Sie die **Create** -Methode, um eine Verbindung mit einem WIA-Hardware Gerät zu erstellen, nachdem Sie die [**Geräte**](-wia-iwia-devices.md) Sammlung aufgelistet haben.</span><span class="sxs-lookup"><span data-stu-id="c91ab-112">Use the **Create** method to create a connection to a WIA hardware device after enumerating the [**Devices**](-wia-iwia-devices.md) collection.</span></span> <span data-ttu-id="c91ab-113">Die-Methode gibt ein [**Item**](-wia-item.md) -Objekt zurück, das das Gerät darstellt (ein root-Element).</span><span class="sxs-lookup"><span data-stu-id="c91ab-113">The method returns an [**Item**](-wia-item.md) object that represents the device (a root item).</span></span>

## <a name="examples"></a><span data-ttu-id="c91ab-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c91ab-114">Examples</span></span>

<span data-ttu-id="c91ab-115">Im folgenden Beispiel wird die Verwendung der **Create** -Methode veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c91ab-115">The following example demonstrates the use of the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="c91ab-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c91ab-116">Requirements</span></span>



| <span data-ttu-id="c91ab-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c91ab-117">Requirement</span></span> | <span data-ttu-id="c91ab-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c91ab-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c91ab-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c91ab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c91ab-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c91ab-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c91ab-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c91ab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c91ab-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c91ab-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c91ab-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c91ab-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c91ab-124"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c91ab-124"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




