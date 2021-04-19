---
description: Tragbare Windows-Geräte unterstützen die folgenden Ressourcen Attribut Eigenschaften.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Eigenschaften des Ressourcen Attributs (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356052"
---
# <a name="resource-attribute-properties"></a><span data-ttu-id="ae8a7-103">Eigenschaften des Ressourcen Attributs</span><span class="sxs-lookup"><span data-stu-id="ae8a7-103">Resource Attribute Properties</span></span>

<span data-ttu-id="ae8a7-104">Tragbare Windows-Geräte unterstützen die folgenden Ressourcen Attribut Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-104">Windows Portable Devices supports the following resource attribute properties.</span></span>



| <span data-ttu-id="ae8a7-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ae8a7-105">Property</span></span>                                    | <span data-ttu-id="ae8a7-106">VarType</span><span class="sxs-lookup"><span data-stu-id="ae8a7-106">VarType</span></span>         | <span data-ttu-id="ae8a7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae8a7-107">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8a7-108">**Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ae8a7-108">**WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY**</span></span> | <span data-ttu-id="ae8a7-109">**VT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="ae8a7-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="ae8a7-110">Dies ist eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) , die einen einzelnen Wert enthält. Dies ist der Schlüssel, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-110">This is an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value, which is the key identifying the resource.</span></span>                     |
| <span data-ttu-id="ae8a7-111">**WPD- \_ Ressourcen \_ Attribut \_ Format**</span><span class="sxs-lookup"><span data-stu-id="ae8a7-111">**WPD\_RESOURCE\_ATTRIBUTE\_FORMAT**</span></span>        | <span data-ttu-id="ae8a7-112">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="ae8a7-112">**VT\_CLSID**</span></span>   | <span data-ttu-id="ae8a7-113">Ein GUID-Wert, der das Format der Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-113">A GUID value that specifies the format of the resource.</span></span> <span data-ttu-id="ae8a7-114">Eine Liste der Formate, die von tragbaren Windows-Geräten definiert werden, finden Sie unter [Objekt Formate](object-format-guids.md) .</span><span class="sxs-lookup"><span data-stu-id="ae8a7-114">See [Object Formats](object-format-guids.md) for a list of formats that are defined by Windows Portable Devices.</span></span> |
| <span data-ttu-id="ae8a7-115">**Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ae8a7-115">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>   | <span data-ttu-id="ae8a7-116">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="ae8a7-116">**VT\_UI8**</span></span>     | <span data-ttu-id="ae8a7-117">Die Gesamtgröße der Ressourcen Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-117">The total size of the resource data, in bytes.</span></span>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ae8a7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae8a7-118">Remarks</span></span>

<span data-ttu-id="ae8a7-119">Diese Attribute werden von der [**iportabledeviceresources:: getresourceattributormethode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-119">These attributes are returned by the [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae8a7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae8a7-120">Requirements</span></span>



| <span data-ttu-id="ae8a7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae8a7-121">Requirement</span></span> | <span data-ttu-id="ae8a7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ae8a7-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8a7-123">Header</span><span class="sxs-lookup"><span data-stu-id="ae8a7-123">Header</span></span><br/> | <dl> <span data-ttu-id="ae8a7-124"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae8a7-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae8a7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae8a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae8a7-126">**Iportabledeviceresources:: getresourceattribute**</span><span class="sxs-lookup"><span data-stu-id="ae8a7-126">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[<span data-ttu-id="ae8a7-127">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="ae8a7-127">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




