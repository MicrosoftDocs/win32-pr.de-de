---
description: Die Create-Methode des Wia-Objekts stellt eine Verbindung mit dem angegebenen WIA-Gerät (Windows Image Acquisition) her und gibt ein Item-Objekt zurück, das das Gerät darstellt.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Wia.Create-Methode
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
ms.openlocfilehash: d22d45e473cec1d5186c300f97cbdb4661237ab9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841331"
---
# <a name="wiacreate-method"></a><span data-ttu-id="df6cd-103">Wia.Create-Methode</span><span class="sxs-lookup"><span data-stu-id="df6cd-103">Wia.Create method</span></span>

<span data-ttu-id="df6cd-104">Die **Create-Methode** des [**Wia-Objekts**](-wia-wia.md) stellt eine Verbindung mit dem angegebenen WIA-Gerät (Windows Image Acquisition) her und gibt ein [**Item-Objekt**](-wia-item.md) zurück, das das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="df6cd-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df6cd-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="df6cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df6cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6cd-107">*Gerät* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="df6cd-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6cd-108">Typ: **\* VARIANT**</span><span class="sxs-lookup"><span data-stu-id="df6cd-108">Type: **VARIANT\***</span></span>

<span data-ttu-id="df6cd-109">Gibt das WIA-Gerät an, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="df6cd-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6cd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df6cd-110">Return value</span></span>

<span data-ttu-id="df6cd-111">Typ: **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="df6cd-111">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="df6cd-112">Bei Erfolg gibt diese Methode ein [**Item-Objekt**](-wia-item.md) zurück, das ein WIA-Hardwaregerät (ein Stammelement) darstellt.</span><span class="sxs-lookup"><span data-stu-id="df6cd-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="df6cd-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df6cd-113">Remarks</span></span>

<span data-ttu-id="df6cd-114">Der *Device-Parameter* gibt ein [**DeviceInfo-Objekt**](-wia-deviceinfo.md) an, indem er das Objekt selbst, seinen Index aus einem Auflistungsobjekt oder den Wert seiner [**ID-Eigenschaft**](-wia-iwiadeviceinfo-id.md) übergibt.</span><span class="sxs-lookup"><span data-stu-id="df6cd-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="df6cd-115">**Nichts** übergeben, um ein Dialogfeld anzuzeigen, in dem ein Benutzer ein Gerät auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="df6cd-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="df6cd-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df6cd-116">Examples</span></span>

<span data-ttu-id="df6cd-117">Die folgenden VBScript-Beispiele veranschaulichen die Verwendung der **Create-Methode.**</span><span class="sxs-lookup"><span data-stu-id="df6cd-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="df6cd-118">Im ersten Beispiel wird ein [**DeviceInfo-Objekt**](-wia-deviceinfo.md) an die **Create-Methode** übergeben.</span><span class="sxs-lookup"><span data-stu-id="df6cd-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="df6cd-119">Beachten Sie, dass die Übergabe der [**ID-Eigenschaft**](-wia-iwiadeviceinfo-id.md) des Objekts genau das gleiche Verhalten verursacht.</span><span class="sxs-lookup"><span data-stu-id="df6cd-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


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



<span data-ttu-id="df6cd-120">Im nächsten Beispiel übergibt die aufrufende Anwendung den Index des [**DeviceInfo-Objekts**](-wia-deviceinfo.md) in der Auflistung an die **Create-Methode.**</span><span class="sxs-lookup"><span data-stu-id="df6cd-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


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



<span data-ttu-id="df6cd-121">Im nächsten Beispiel wird **Nothing** an die **Create-Methode** übergeben, um ein Dialogfeld anzuzeigen, in dem ein Benutzer ein Gerät auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="df6cd-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="df6cd-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df6cd-122">Requirements</span></span>



| <span data-ttu-id="df6cd-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df6cd-123">Requirement</span></span> | <span data-ttu-id="df6cd-124">Wert</span><span class="sxs-lookup"><span data-stu-id="df6cd-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df6cd-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df6cd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="df6cd-126">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df6cd-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df6cd-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df6cd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="df6cd-128">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df6cd-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="df6cd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="df6cd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df6cd-130"><dt>Wiascr.dll (Version 4.90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="df6cd-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




