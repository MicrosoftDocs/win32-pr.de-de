---
description: Die Create-Methode des WIA-Objekts stellt eine Verbindung mit dem angegebenen Windows-Abbild Erfassungsgerät (WIA) her und gibt ein Element Objekt zurück, das das Gerät darstellt.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: WIA. Create-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529150"
---
# <a name="wiacreate-method"></a><span data-ttu-id="cd9ac-103">WIA. Create-Methode</span><span class="sxs-lookup"><span data-stu-id="cd9ac-103">Wia.Create method</span></span>

<span data-ttu-id="cd9ac-104">Die **Create** -Methode des [**WIA**](-wia-wia.md) -Objekts stellt eine Verbindung mit dem angegebenen Windows-Abbild Erfassungsgerät (WIA) her und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd9ac-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="cd9ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd9ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd9ac-107">*Gerät* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd9ac-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9ac-108">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="cd9ac-108">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="cd9ac-109">Gibt das WIA-Gerät an, mit dem eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd9ac-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd9ac-110">Return value</span></span>

<span data-ttu-id="cd9ac-111">Typ: _ *iwiadispatchitem*\*</span><span class="sxs-lookup"><span data-stu-id="cd9ac-111">Type: _ *IWiaDispatchItem*\*</span></span>

<span data-ttu-id="cd9ac-112">Bei erfolgreicher Ausführung gibt diese Methode ein [**Element**](-wia-item.md) Objekt zurück, das ein WIA-Hardware Gerät (ein Stamm Element) darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd9ac-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd9ac-113">Remarks</span></span>

<span data-ttu-id="cd9ac-114">Der *Geräte* Parameter gibt ein Objekt vom Typ " [**toviceinfo**](-wia-deviceinfo.md) " an, indem das Objekt selbst, dessen Index von einem Auflistungs Objekt oder der Wert der [**ID**](-wia-iwiadeviceinfo-id.md) -Eigenschaft übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="cd9ac-115">Übergeben Sie **nichts** , um ein Dialogfeld anzuzeigen, das einem Benutzer ermöglicht, ein Gerät auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="cd9ac-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd9ac-116">Examples</span></span>

<span data-ttu-id="cd9ac-117">Die folgenden VBScript-Beispiele veranschaulichen die Verwendung der **Create** -Methode.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="cd9ac-118">Im ersten Beispiel wird ein [**deviceInfo**](-wia-deviceinfo.md) -Objekt an die **Create** -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="cd9ac-119">Beachten Sie, dass das übergeben der [**ID**](-wia-iwiadeviceinfo-id.md) -Eigenschaft des Objekts genau dasselbe Verhalten bewirkt.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



<span data-ttu-id="cd9ac-120">Im nächsten Beispiel übergibt die aufrufenden Anwendung den Index des [**deviceInfo**](-wia-deviceinfo.md) -Objekts in der-Auflistung an die **Create** -Methode.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



<span data-ttu-id="cd9ac-121">Das nächste Beispiel übergibt **nichts** an die **Create** -Methode, um ein Dialogfeld anzuzeigen, in dem ein Benutzer ein Gerät auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="cd9ac-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="cd9ac-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd9ac-122">Requirements</span></span>



| <span data-ttu-id="cd9ac-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd9ac-123">Requirement</span></span> | <span data-ttu-id="cd9ac-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cd9ac-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9ac-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd9ac-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd9ac-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd9ac-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd9ac-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd9ac-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd9ac-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd9ac-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cd9ac-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cd9ac-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd9ac-130"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ac-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




