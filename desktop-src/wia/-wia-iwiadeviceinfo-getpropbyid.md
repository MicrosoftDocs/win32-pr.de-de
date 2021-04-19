---
description: Die getpropbyid-Methode des DeviceInfo-Objekts verwendet die ID einer Geräte Eigenschaft, um ihren Wert zurückzugeben.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Deviceingefo. getpropbyid-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350238"
---
# <a name="deviceinfogetpropbyid-method"></a><span data-ttu-id="50dd0-103">Deviceingefo. getpropbyid-Methode</span><span class="sxs-lookup"><span data-stu-id="50dd0-103">DeviceInfo.GetPropById method</span></span>

<span data-ttu-id="50dd0-104">Die **getpropbyid** -Methode des [**deviceInfo**](-wia-deviceinfo.md) -Objekts verwendet die ID einer Geräte Eigenschaft, um ihren Wert zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="50dd0-104">The **GetPropById** method of the [**DeviceInfo**](-wia-deviceinfo.md) object uses a device property's ID to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="50dd0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50dd0-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="50dd0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50dd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50dd0-107">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50dd0-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50dd0-108">Typ: **[wiadeviceinf opropertyid](-wia-wiadeviceinfopropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="50dd0-108">Type: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span></span>

<span data-ttu-id="50dd0-109">Gibt die ID der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="50dd0-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50dd0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50dd0-110">Return value</span></span>

<span data-ttu-id="50dd0-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="50dd0-111">Type: **VARIANT**</span></span>

<span data-ttu-id="50dd0-112">Diese Methode gibt den Wert der Eigenschaft zurück, die durch *ID* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="50dd0-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="50dd0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50dd0-113">Remarks</span></span>

<span data-ttu-id="50dd0-114">Verwenden Sie diese Methode, um den Wert einer Geräte Eigenschaft aus der ID zu suchen.</span><span class="sxs-lookup"><span data-stu-id="50dd0-114">Use this method to find the value of a device property from its ID.</span></span> <span data-ttu-id="50dd0-115">Eine Liste der Eigenschaften-IDs finden Sie unter [Eigenschaften konstanter Definitionen von WIA](-wia-wia-property-constant-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="50dd0-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="50dd0-116">Weitere Informationen zu den Eigenschaften der Windows-Abbild Erfassung (WIA) selbst finden Sie unter [WIA Property Konstanten](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="50dd0-116">For information about Windows Image Acquisition (WIA) properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="50dd0-117">Fügen Sie für Microsoft Visual Basic-Anwendungen einen Verweis auf die Typbibliothek "Windows-Abbild Erfassung 1,01" hinzu.</span><span class="sxs-lookup"><span data-stu-id="50dd0-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="50dd0-118">Die folgenden Konstanten, die in dieser Datei definiert sind, sind für diese Methode gültig:</span><span class="sxs-lookup"><span data-stu-id="50dd0-118">This following constants defined in that file are valid for this method:</span></span>

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a><span data-ttu-id="50dd0-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50dd0-119">Examples</span></span>

<span data-ttu-id="50dd0-120">Im folgenden Beispiel wird veranschaulicht, wie die **getpropbyid** -Methode verwendet wird, um einen Eigenschafts Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50dd0-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="50dd0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50dd0-121">Requirements</span></span>



| <span data-ttu-id="50dd0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50dd0-122">Requirement</span></span> | <span data-ttu-id="50dd0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="50dd0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dd0-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50dd0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="50dd0-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50dd0-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50dd0-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50dd0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="50dd0-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50dd0-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="50dd0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="50dd0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50dd0-129"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="50dd0-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




