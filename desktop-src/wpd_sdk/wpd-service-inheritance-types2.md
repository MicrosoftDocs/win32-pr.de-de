---
description: Gibt die Vererbungs Beziehung für einen Dienst an.
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: WPD_SERVICE_INHERITANCE_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ad9115bf7bb0912362455986e77d5792cceec3b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369565"
---
# <a name="wpd_service_inheritance_types-enumeration"></a><span data-ttu-id="9157e-103">\_ \_ Enumeration der Vererbungs \_ Typen für WPD-Dienste</span><span class="sxs-lookup"><span data-stu-id="9157e-103">WPD\_SERVICE\_INHERITANCE\_TYPES enumeration</span></span>

<span data-ttu-id="9157e-104">Der Enumerationstyp der **WPD- \_ Dienst \_ Vererbung \_** gibt die Vererbungs Beziehung für einen Dienst an.</span><span class="sxs-lookup"><span data-stu-id="9157e-104">The **WPD\_SERVICE\_INHERITANCE\_TYPES** enumeration type specifies the inheritance relationship for a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9157e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9157e-105">Syntax</span></span>


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="9157e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9157e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9157e-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**Implementierung der WPD- \_ Dienst \_ Vererbung \_**</span><span class="sxs-lookup"><span data-stu-id="9157e-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**WPD\_SERVICE\_INHERITANCE\_IMPLEMENTATION**</span></span>
</dt> <dd>

<span data-ttu-id="9157e-108">Der Dienst erbt, indem er eine abstrakte Dienst Definition implementiert.</span><span class="sxs-lookup"><span data-stu-id="9157e-108">The service inherits by implementing an abstract service definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9157e-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9157e-109">Requirements</span></span>



| <span data-ttu-id="9157e-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9157e-110">Requirement</span></span> | <span data-ttu-id="9157e-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9157e-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9157e-112">Header</span><span class="sxs-lookup"><span data-stu-id="9157e-112">Header</span></span><br/> | <dl> <span data-ttu-id="9157e-113"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9157e-113"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9157e-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9157e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9157e-115">**Iportabletviceservicecapabili:: getinheritedservices**</span><span class="sxs-lookup"><span data-stu-id="9157e-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




