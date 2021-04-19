---
description: 'Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für die Methoden eines Geräte Dienstanbieter. Diese Attribute werden von der iportabledeviceservicecapabili:: getmethodattributes-Methode zurückgegeben.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Methoden Attribute (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370044"
---
# <a name="method-attributes"></a><span data-ttu-id="5f927-104">Methodenattribut</span><span class="sxs-lookup"><span data-stu-id="5f927-104">Method Attributes</span></span>

<span data-ttu-id="5f927-105">Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für die Methoden eines Geräte Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="5f927-105">For Windows 7, Windows Portable Devices supports the following attributes for methods of a device service.</span></span> <span data-ttu-id="5f927-106">Diese Attribute werden von der [**iportabledeviceservicecapabili:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f927-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method.</span></span>




| <span data-ttu-id="5f927-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="5f927-107">Attribute</span></span>                                      | <span data-ttu-id="5f927-108">VarType</span><span class="sxs-lookup"><span data-stu-id="5f927-108">VarType</span></span>         | <span data-ttu-id="5f927-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f927-109">Description</span></span>                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f927-110">**Zugriff auf WPD- \_ Methoden \_ Attribut \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-110">**WPD\_METHOD\_ATTRIBUTE\_ACCESS**</span></span>             | <span data-ttu-id="5f927-111">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="5f927-111">**VT\_CLSID**</span></span>   | <span data-ttu-id="5f927-112">Der erforderliche Methoden Zugriff.</span><span class="sxs-lookup"><span data-stu-id="5f927-112">The required method access.</span></span>                                                                                               |
| <span data-ttu-id="5f927-113">**mit dem WPD- \_ Methoden \_ Attribut \_ verknüpfte \_ Format**</span><span class="sxs-lookup"><span data-stu-id="5f927-113">**WPD\_METHOD\_ATTRIBUTE\_ASSOCIATED\_FORMAT**</span></span> | <span data-ttu-id="5f927-114">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="5f927-114">**VT\_CLSID**</span></span>   | <span data-ttu-id="5f927-115">Das Format, das der Methode zugeordnet ist, oder **GUID \_ null** , wenn kein zugeordnetes Format vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5f927-115">The format associated with the method, or **GUID\_NULL** if there is no associated format.</span></span>                                |
| <span data-ttu-id="5f927-116">**\_ \_ Attribut \_ Name der WPD-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f927-116">**WPD\_METHOD\_ATTRIBUTE\_NAME**</span></span>               | <span data-ttu-id="5f927-117">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5f927-117">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="5f927-118">Eine Zeichenfolge, die den Skript freundlichen Namen der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="5f927-118">A string that specifies the script-friendly name of the method.</span></span> <span data-ttu-id="5f927-119">Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="5f927-119">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="5f927-120">**\_ \_ Attribut \_ Parameter für WPD-Methoden**</span><span class="sxs-lookup"><span data-stu-id="5f927-120">**WPD\_METHOD\_ATTRIBUTE\_PARAMETERS**</span></span>         | <span data-ttu-id="5f927-121">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="5f927-121">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="5f927-122">Eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) -Schnittstelle, die die Methoden Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="5f927-122">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that contains the method parameters.</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="5f927-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f927-123">Requirements</span></span>



| <span data-ttu-id="5f927-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f927-124">Requirement</span></span> | <span data-ttu-id="5f927-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5f927-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f927-126">Header</span><span class="sxs-lookup"><span data-stu-id="5f927-126">Header</span></span><br/> | <dl> <span data-ttu-id="5f927-127"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f927-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f927-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f927-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f927-129">**Eigenschaften und Attribute**</span><span class="sxs-lookup"><span data-stu-id="5f927-129">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




