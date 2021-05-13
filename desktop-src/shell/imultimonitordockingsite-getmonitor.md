---
description: Ruft den aktuellen Standardmonitor ab.
title: IMultiMonitorDockingSite::GetMonitor-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840641"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="8b5de-103">IMultiMonitorDockingSite::GetMonitor-Methode</span><span class="sxs-lookup"><span data-stu-id="8b5de-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="8b5de-104">Ruft den aktuellen Standardmonitor ab.</span><span class="sxs-lookup"><span data-stu-id="8b5de-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b5de-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="8b5de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b5de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5de-107">*dateiSrc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8b5de-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5de-108">Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="8b5de-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="8b5de-109">Ein Zeiger auf das Objekt, das die [**IDockingWindow-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) implementiert, für die der Monitor angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="8b5de-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="8b5de-110">*phMon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b5de-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5de-111">Typ: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="8b5de-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="8b5de-112">Wenn die Funktion zurückgegeben wird, enthält sie einen Zeiger auf das Handle des Standardmonitors.</span><span class="sxs-lookup"><span data-stu-id="8b5de-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5de-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b5de-113">Return value</span></span>

<span data-ttu-id="8b5de-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b5de-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8b5de-115">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="8b5de-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b5de-116">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b5de-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5de-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b5de-117">Requirements</span></span>



| <span data-ttu-id="8b5de-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b5de-118">Requirement</span></span> | <span data-ttu-id="8b5de-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8b5de-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="8b5de-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b5de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8b5de-121">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b5de-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8b5de-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b5de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8b5de-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b5de-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
