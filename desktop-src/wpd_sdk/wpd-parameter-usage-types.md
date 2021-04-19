---
description: Der \_ Enumerationstyp der WPD-Parameter \_ Verwendungs \_ Typen beschreibt, wie ein Methoden Parameter in einer bestimmten Methode verwendet wird.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: WPD_PARAMETER_USAGE_TYPES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367642"
---
# <a name="wpd_parameter_usage_types-enumeration"></a><span data-ttu-id="1fc26-103">WPD- \_ Parameter \_ Verwendungs Typen- \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="1fc26-103">WPD\_PARAMETER\_USAGE\_TYPES enumeration</span></span>

<span data-ttu-id="1fc26-104">Der Enumerationstyp der [**WPD- \_ Parameter \_ Verwendungs \_ Typen**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) beschreibt, wie ein Methoden Parameter in einer bestimmten Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fc26-104">The [**WPD\_PARAMETER\_USAGE\_TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) enumeration type describes how a method parameter is used in a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fc26-105">Syntax</span></span>


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="1fc26-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1fc26-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1fc26-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**Verwendungs Rückgabe von WPD- \_ Parametern \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1fc26-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD\_PARAMETER\_USAGE\_RETURN**</span></span>
</dt> <dd>

<span data-ttu-id="1fc26-108">Der-Parameter empfängt den Rückgabewert, wenn er von der-Methode angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1fc26-108">The parameter receives the return value, if specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="1fc26-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**Verwendung von WPD- \_ Parametern \_ \_ in**</span><span class="sxs-lookup"><span data-stu-id="1fc26-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD\_PARAMETER\_USAGE\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="1fc26-110">Der-Parameter enthält einen Eingabe Wert, bevor die-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1fc26-110">The parameter contains an input value before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="1fc26-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**Verwendung von WPD- \_ Parametern \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1fc26-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD\_PARAMETER\_USAGE\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="1fc26-112">Der-Parameter enthält einen Ausgabewert, wenn die-Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1fc26-112">The parameter contains an output value when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="1fc26-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_ \_ INOUT-Verwendung \_ von WPD-Parametern**</span><span class="sxs-lookup"><span data-stu-id="1fc26-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD\_PARAMETER\_USAGE\_INOUT**</span></span>
</dt> <dd>

<span data-ttu-id="1fc26-114">Der-Parameter enthält einen Eingabe Wert, bevor die-Methode aufgerufen wird, und einen Ausgabewert, wenn Sie zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1fc26-114">The parameter contains an input value before the method is called and an output value when it returns.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fc26-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fc26-115">Requirements</span></span>



| <span data-ttu-id="1fc26-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fc26-116">Requirement</span></span> | <span data-ttu-id="1fc26-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1fc26-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc26-118">Header</span><span class="sxs-lookup"><span data-stu-id="1fc26-118">Header</span></span><br/> | <dl> <span data-ttu-id="1fc26-119"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fc26-119"><dt>PortableDevice.h</dt></span></span> </dl> |



 

