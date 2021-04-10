---
description: Die dllgetmonitorobject-Funktion muss vom Monitor implementiert werden. Die mcsvc ruft diese Funktion auf, um eine Instanz des Monitors zu erstellen.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Dllgetmonitorobject-Rückruffunktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868223"
---
# <a name="dllgetmonitorobject-callback-function"></a><span data-ttu-id="1e619-104">Dllgetmonitorobject-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="1e619-104">DllGetMonitorObject callback function</span></span>

<span data-ttu-id="1e619-105">Die **dllgetmonitorobject** -Funktion muss vom Monitor implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e619-105">The **DllGetMonitorObject** function must be implemented by the monitor.</span></span> <span data-ttu-id="1e619-106">Die mcsvc ruft diese Funktion auf, um eine Instanz des Monitors zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e619-106">The MCSVC calls this function to create an instance of the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e619-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e619-107">Syntax</span></span>


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="1e619-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e619-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e619-109">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e619-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e619-110">UUID der unten gezeigten Monitore, wie in der Header Datei "imonitor. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="1e619-110">UUID of monitors, shown below, as defined in the IMonitor.h header file.</span></span> <span data-ttu-id="1e619-111">Wenn eine ungültige UUID bereitgestellt wird, schlägt die Funktion fehl, und der Monitor muss E \_ nointerface zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e619-111">If an invalid UUID is provided, the function fails, and the monitor must return E\_NOINTERFACE.</span></span>

``` syntax
IID_IMonitor
```

</dd> <dt>

<span data-ttu-id="1e619-112">*ppobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1e619-112">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e619-113">Zeiger auf einen Zeiger, der die in *riid* angeforderte Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="1e619-113">Pointer to a pointer that receives the interface requested in *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e619-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e619-114">Return value</span></span>

<span data-ttu-id="1e619-115">Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK (entspricht noError).</span><span class="sxs-lookup"><span data-stu-id="1e619-115">If the function is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="1e619-116">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1e619-116">If the function is unsuccessful, the return value is a failure code.</span></span> <span data-ttu-id="1e619-117">Wenn ein Fehlercode zurückgegeben wird, erstellt das mcsvc das Monitor Objekt nicht, und die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode wird nicht für den Schnittstellen Zeiger aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e619-117">When a failure code is returned, the MCSVC does not create the monitor object, and the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method is not called on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e619-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e619-118">Remarks</span></span>

<span data-ttu-id="1e619-119">Die **dllgetmonitorobject** -Funktion wird jedes Mal aufgerufen, wenn der mcsvc versucht, eine Instanz des Monitors zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e619-119">The **DllGetMonitorObject** function is called each time the MCSVC tries to create an instance of the monitor.</span></span> <span data-ttu-id="1e619-120">Diese Funktion weist absichtlich eine starke Ähnlichkeit mit der gängigeren [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="1e619-120">This function intentionally bears a strong resemblance to the more common [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) function.</span></span> <span data-ttu-id="1e619-121">Der Hauptunterschied besteht darin, dass eine CLSID nicht an **dllgetmonitorobject** übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="1e619-121">The main difference is that a CLSID is not passed in to **DllGetMonitorObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e619-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e619-122">Requirements</span></span>



| <span data-ttu-id="1e619-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e619-123">Requirement</span></span> | <span data-ttu-id="1e619-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1e619-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1e619-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e619-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1e619-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e619-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1e619-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e619-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1e619-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e619-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1e619-129">Header</span><span class="sxs-lookup"><span data-stu-id="1e619-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e619-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e619-130"><dt>Netmon.h</dt></span></span> </dl> |



 

