---
description: Der \_ \_ Enumerationstyp "Objekt Optionen löschen" beschreibt Optionen, die beim Löschen eines Objekts von einem Gerät unterstützt werden.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: DELETE_OBJECT_OPTIONS-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368567"
---
# <a name="delete_object_options-enumeration"></a><span data-ttu-id="7d250-103">\_Objekt \_ Optionen-Enumeration löschen</span><span class="sxs-lookup"><span data-stu-id="7d250-103">DELETE\_OBJECT\_OPTIONS enumeration</span></span>

<span data-ttu-id="7d250-104">Der Enumerationstyp " **\_ Objekt \_ Optionen löschen** " beschreibt Optionen, die beim Löschen eines Objekts von einem Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7d250-104">The **DELETE\_OBJECT\_OPTIONS** enumeration type describes options that are supported by a device when deleting an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d250-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d250-105">Syntax</span></span>


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="7d250-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7d250-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d250-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**Portable \_ Geräte \_ Delete \_ keine \_ Rekursion**</span><span class="sxs-lookup"><span data-stu-id="7d250-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_NO\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="7d250-108">Löschen Sie das Objekt nur, und schlagen Sie fehl, wenn es untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d250-108">Delete the object only and fail if it has children.</span></span>

</dd> <dt>

<span data-ttu-id="7d250-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_Löschen von portablen Geräten \_ \_ mit \_ Rekursion**</span><span class="sxs-lookup"><span data-stu-id="7d250-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_WITH\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="7d250-110">Löschen Sie das-Objekt und alle zugehörigen untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="7d250-110">Delete the object and all its children.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d250-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d250-111">Remarks</span></span>

<span data-ttu-id="7d250-112">Die Anwendung kann die Lösch Optionen abrufen, die das Gerät unterstützt, indem [**iportabledevicecapabili:: getcommandoptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) für den Befehl **WPD \_ Command \_ Object \_ Management \_ Delete \_ Objects** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7d250-112">The application can retrieve the deletion options that the device supports by calling [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) for the **WPD\_COMMAND\_OBJECT\_MANAGEMENT\_DELETE\_OBJECTS** command.</span></span> <span data-ttu-id="7d250-113">Der Wert für die Option " **\_ \_ \_ \_ rekursiver Löschvorgang \_ \_ unterstützt** ", der von dieser Methode in einem [**iportabledevicevaluescollection**](iportabledevicevaluescollection.md) -Objekt zurückgegeben wird, sollte untersucht werden.</span><span class="sxs-lookup"><span data-stu-id="7d250-113">It should examine the **WPD\_OPTION\_OBJECT\_MANAGEMENT\_RECURSIVE\_DELETE\_SUPPORTED** option value that this method returns in an [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d250-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d250-114">Requirements</span></span>



| <span data-ttu-id="7d250-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d250-115">Requirement</span></span> | <span data-ttu-id="7d250-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7d250-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d250-117">Header</span><span class="sxs-lookup"><span data-stu-id="7d250-117">Header</span></span><br/> | <dl> <span data-ttu-id="7d250-118"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d250-118"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d250-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d250-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d250-120">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="7d250-120">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




