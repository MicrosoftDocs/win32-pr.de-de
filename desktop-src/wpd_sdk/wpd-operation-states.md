---
description: Der WPD-Vorgang gibt an, dass \_ \_ Enumerationswerte den aktuellen Status eines aktuell ausgeführten Vorgangs beschreiben.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: WPD_OPERATION_STATES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361372"
---
# <a name="wpd_operation_states-enumeration"></a><span data-ttu-id="9c093-103">WPD- \_ Operation \_ States-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9c093-103">WPD\_OPERATION\_STATES enumeration</span></span>

<span data-ttu-id="9c093-104">Der **WPD \_ - \_ Vorgang** gibt an, dass Enumerationswerte den aktuellen Status eines aktuell ausgeführten Vorgangs beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9c093-104">The **WPD\_OPERATION\_STATES** enumeration values describe the current state of an operation in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c093-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c093-105">Syntax</span></span>


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a><span data-ttu-id="9c093-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9c093-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9c093-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**der WPD- \_ Vorgangs \_ Status ist \_ nicht angegeben.**</span><span class="sxs-lookup"><span data-stu-id="9c093-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**WPD\_OPERATION\_STATE\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="9c093-108">Der aktuelle Vorgang befindet sich in einem nicht angegebenen Zustand (nicht festgelegt) und ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="9c093-108">The current operation is in an unspecified state (not set) and unknown.</span></span>

</dd> <dt>

<span data-ttu-id="9c093-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD- \_ Vorgangs \_ Status wurde \_ gestartet.**</span><span class="sxs-lookup"><span data-stu-id="9c093-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD\_OPERATION\_STATE\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="9c093-110">Der Vorgang wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="9c093-110">The operation is started.</span></span>

</dd> <dt>

<span data-ttu-id="9c093-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD- \_ Vorgangs \_ Status wird \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="9c093-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD\_OPERATION\_STATE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="9c093-112">Der Vorgang wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c093-112">The operation is running.</span></span>

</dd> <dt>

<span data-ttu-id="9c093-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD- \_ Vorgangs \_ Status \_ angehalten**</span><span class="sxs-lookup"><span data-stu-id="9c093-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD\_OPERATION\_STATE\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="9c093-114">Der Vorgang wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="9c093-114">The operation is paused.</span></span>

</dd> <dt>

<span data-ttu-id="9c093-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD- \_ Vorgangs \_ Status \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="9c093-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD\_OPERATION\_STATE\_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="9c093-116">Der Vorgang wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9c093-116">The operation is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="9c093-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD- \_ Vorgangs \_ Status \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="9c093-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD\_OPERATION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="9c093-118">Der Vorgang ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9c093-118">The operation is finished.</span></span>

</dd> <dt>

<span data-ttu-id="9c093-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD- \_ Vorgangs \_ Status \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="9c093-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD\_OPERATION\_STATE\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="9c093-120">Der Vorgang wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9c093-120">The operation is aborted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c093-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c093-121">Remarks</span></span>

<span data-ttu-id="9c093-122">Diese Werte werden im Anwendungs definierten Rückruf ([**iportabledeviceeventcallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)) empfangen.</span><span class="sxs-lookup"><span data-stu-id="9c093-122">These values are received in the application-defined callback ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c093-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c093-123">Requirements</span></span>



| <span data-ttu-id="9c093-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c093-124">Requirement</span></span> | <span data-ttu-id="9c093-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9c093-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c093-126">Header</span><span class="sxs-lookup"><span data-stu-id="9c093-126">Header</span></span><br/> | <dl> <span data-ttu-id="9c093-127"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c093-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c093-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c093-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c093-129">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="9c093-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




