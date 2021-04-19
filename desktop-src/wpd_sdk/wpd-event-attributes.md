---
description: 'Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für Ereignisse eines Geräte Dienstanbieter. Diese Attribute werden von der iportabledeviceservicecapabili:: geteventattributormethode zurückgegeben.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Ereignis Attribute (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373574"
---
# <a name="event-attributes-portabledeviceh"></a><span data-ttu-id="708b4-104">Ereignis Attribute (portabledevice. h)</span><span class="sxs-lookup"><span data-stu-id="708b4-104">Event Attributes (PortableDevice.h)</span></span>

<span data-ttu-id="708b4-105">Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für Ereignisse eines Geräte Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="708b4-105">For Windows 7, Windows Portable Devices supports the following attributes for events of a device service.</span></span> <span data-ttu-id="708b4-106">Diese Attribute werden von der [**iportabledeviceservicecapabili:: geteventattributormethode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="708b4-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method.</span></span>




| <span data-ttu-id="708b4-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="708b4-107">Attribute</span></span>                             | <span data-ttu-id="708b4-108">VarType</span><span class="sxs-lookup"><span data-stu-id="708b4-108">VarType</span></span>         | <span data-ttu-id="708b4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="708b4-109">Description</span></span>                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="708b4-110">**Name des WPD- \_ Ereignis \_ Attributs \_**</span><span class="sxs-lookup"><span data-stu-id="708b4-110">**WPD\_EVENT\_ATTRIBUTE\_NAME**</span></span>       | <span data-ttu-id="708b4-111">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="708b4-111">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="708b4-112">Eine Zeichenfolge, die den Skript freundlichen Namen des Ereignisses angibt.</span><span class="sxs-lookup"><span data-stu-id="708b4-112">A string that specifies the script-friendly name of the event.</span></span> <span data-ttu-id="708b4-113">Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="708b4-113">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="708b4-114">**Optionen für das WPD- \_ Ereignis \_ Attribut \_**</span><span class="sxs-lookup"><span data-stu-id="708b4-114">**WPD\_EVENT\_ATTRIBUTE\_OPTIONS**</span></span>    | <span data-ttu-id="708b4-115">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="708b4-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="708b4-116">Ein [**iportabledevicevalues**](iportabledevicevalues.md) -Element, das die Ereignis Optionen enthält.</span><span class="sxs-lookup"><span data-stu-id="708b4-116">An [**IPortableDeviceValues**](iportabledevicevalues.md) that contains the event options.</span></span>                               |
| <span data-ttu-id="708b4-117">**Parameter für WPD- \_ Ereignis \_ Attribute \_**</span><span class="sxs-lookup"><span data-stu-id="708b4-117">**WPD\_EVENT\_ATTRIBUTE\_PARAMETERS**</span></span> | <span data-ttu-id="708b4-118">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="708b4-118">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="708b4-119">Eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) , die die Ereignis Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="708b4-119">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) that contains the event parameters.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="708b4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="708b4-120">Requirements</span></span>



| <span data-ttu-id="708b4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="708b4-121">Requirement</span></span> | <span data-ttu-id="708b4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="708b4-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="708b4-123">Header</span><span class="sxs-lookup"><span data-stu-id="708b4-123">Header</span></span><br/> | <dl> <span data-ttu-id="708b4-124"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="708b4-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="708b4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="708b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708b4-126">**Eigenschaften und Attribute**</span><span class="sxs-lookup"><span data-stu-id="708b4-126">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




