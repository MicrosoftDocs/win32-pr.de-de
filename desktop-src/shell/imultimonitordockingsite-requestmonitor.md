---
description: Überprüft, ob der Monitor aktiv und verfügbar ist.
title: 'Imultimonitordockingsite:: RequestMonitor-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 5389b10af9aaa3da5d3106d82a4fbdcbd614a094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960945"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="56439-103">Imultimonitordockingsite:: RequestMonitor-Methode</span><span class="sxs-lookup"><span data-stu-id="56439-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="56439-104">Überprüft, ob der Monitor aktiv und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="56439-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="56439-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56439-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="56439-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56439-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56439-107">*punksrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56439-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56439-108">Typ: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="56439-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="56439-109">Ein Zeiger auf das Objekt, das die [_ *idockingwindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="56439-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="56439-110">*phmon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56439-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56439-111">Geben Sie Folgendes ein: \**Hmonitor \** _</span><span class="sxs-lookup"><span data-stu-id="56439-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="56439-112">Ein Zeiger auf das Handle des Standard Monitors.</span><span class="sxs-lookup"><span data-stu-id="56439-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56439-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56439-113">Return value</span></span>

<span data-ttu-id="56439-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="56439-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="56439-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="56439-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56439-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56439-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56439-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="56439-117">Requirements</span></span>



| <span data-ttu-id="56439-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56439-118">Requirement</span></span> | <span data-ttu-id="56439-119">Wert</span><span class="sxs-lookup"><span data-stu-id="56439-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="56439-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56439-120">Minimum supported client</span></span><br/> | <span data-ttu-id="56439-121">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56439-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="56439-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56439-122">Minimum supported server</span></span><br/> | <span data-ttu-id="56439-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56439-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
