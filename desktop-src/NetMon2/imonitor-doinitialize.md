---
description: Die doinitialize-Methode muss vom Monitor implementiert werden. Die mcsvc ruft diese Methode auf, um unmittelbar vor dem Aufrufen der NPPs-Methode "untcconnect" einen Erfassungs Filter zu erhalten.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Imonitordoinitialize-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525115"
---
# <a name="imonitordoinitialize-method"></a><span data-ttu-id="7fd35-104">Imonitor::D oinitialize-Methode</span><span class="sxs-lookup"><span data-stu-id="7fd35-104">IMonitor::DoInitialize method</span></span>

<span data-ttu-id="7fd35-105">Die **doinitialize** -Methode muss vom Monitor implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fd35-105">The **DoInitialize** method must be implemented by the monitor.</span></span> <span data-ttu-id="7fd35-106">Die mcsvc ruft diese Methode auf, um einen Erfassungs Filter direkt vor dem Aufrufen der " [untc:: Connect](irtc-connect.md) "-Methode von NPP abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7fd35-106">The MCSVC calls this method to obtain a capture filter immediately before calling the NPP's [IRTC::Connect](irtc-connect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd35-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fd35-107">Syntax</span></span>


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a><span data-ttu-id="7fd35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fd35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd35-109">*punkmonitorctrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fd35-109">*pUnkMonitorCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd35-110">Ein [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger, der von mcsvc übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="7fd35-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer passed in by the MCSVC.</span></span> <span data-ttu-id="7fd35-111">Um eine unterstützte Monitor Steuerungs Schnittstelle zu erhalten, muss der Monitor [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Zeiger abrufen.</span><span class="sxs-lookup"><span data-stu-id="7fd35-111">To obtain a supported monitor control interface, the monitor must call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer.</span></span>

</dd> <dt>

<span data-ttu-id="7fd35-112">*hnppblob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7fd35-112">*hNPPBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fd35-113">Bei Eingabe ein Handle für ein NPP-BLOB.</span><span class="sxs-lookup"><span data-stu-id="7fd35-113">On input, a handle to an NPP BLOB.</span></span>

<span data-ttu-id="7fd35-114">Bei der Ausgabe ein NPP-BLOB, das einen Erfassungs Filter enthält.</span><span class="sxs-lookup"><span data-stu-id="7fd35-114">On output, an NPP BLOB that contains a capture filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd35-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fd35-115">Return value</span></span>

<span data-ttu-id="7fd35-116">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError).</span><span class="sxs-lookup"><span data-stu-id="7fd35-116">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="7fd35-117">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7fd35-117">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="7fd35-118">Bei einem Fehler erstellt der mcsvc den Monitor nicht, oder der Befehl [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) wird nicht auf dem Schnittstellen Zeiger aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7fd35-118">On error, the MCSVC will not create the monitor or call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd35-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fd35-119">Remarks</span></span>

<span data-ttu-id="7fd35-120">Die mcsvc Ruft die **doinitialize** -Methode auf, um die erforderliche Monitor Initialisierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7fd35-120">The MCSVC calls the **DoInitialize** method to perform any required monitor initialization.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd35-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fd35-121">Requirements</span></span>



| <span data-ttu-id="7fd35-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fd35-122">Requirement</span></span> | <span data-ttu-id="7fd35-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7fd35-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd35-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fd35-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd35-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fd35-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7fd35-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fd35-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd35-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fd35-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7fd35-128">Header</span><span class="sxs-lookup"><span data-stu-id="7fd35-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fd35-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd35-129"><dt>Netmon.h</dt></span></span> </dl> |



 

