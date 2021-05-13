---
description: Überprüft, ob der Monitor aktiv und verfügbar ist.
title: IMultiMonitorDockingSite::RequestMonitor-Methode
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
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841971"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="18bb6-103">IMultiMonitorDockingSite::RequestMonitor-Methode</span><span class="sxs-lookup"><span data-stu-id="18bb6-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="18bb6-104">Überprüft, ob der Monitor aktiv und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="18bb6-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="18bb6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18bb6-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="18bb6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="18bb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18bb6-107">*dateiSrc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="18bb6-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18bb6-108">Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="18bb6-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="18bb6-109">Ein Zeiger auf das Objekt, das die [**IDockingWindow-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) implementiert.</span><span class="sxs-lookup"><span data-stu-id="18bb6-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="18bb6-110">*phMon* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="18bb6-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18bb6-111">Typ: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="18bb6-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="18bb6-112">Ein Zeiger auf das Handle des Standardmonitors.</span><span class="sxs-lookup"><span data-stu-id="18bb6-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18bb6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18bb6-113">Return value</span></span>

<span data-ttu-id="18bb6-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="18bb6-114">Type: **HRESULT**</span></span>

<span data-ttu-id="18bb6-115">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="18bb6-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18bb6-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18bb6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="18bb6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18bb6-117">Requirements</span></span>



| <span data-ttu-id="18bb6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18bb6-118">Requirement</span></span> | <span data-ttu-id="18bb6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="18bb6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="18bb6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18bb6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18bb6-121">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18bb6-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="18bb6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18bb6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18bb6-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18bb6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
