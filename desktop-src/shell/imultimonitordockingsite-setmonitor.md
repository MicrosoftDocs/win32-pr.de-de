---
description: Ändert, welcher Monitor für angedockte Symbolleisten auf einem System mit mehreren Monitoren verwendet wird.
title: IMultiMonitorDockingSite::SetMonitor-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841941"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="d016f-103">IMultiMonitorDockingSite::SetMonitor-Methode</span><span class="sxs-lookup"><span data-stu-id="d016f-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="d016f-104">Ändert, welcher Monitor für angedockte Symbolleisten auf einem System mit mehreren Monitoren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d016f-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d016f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d016f-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="d016f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d016f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d016f-107">*hexSrc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d016f-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d016f-108">Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="d016f-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="d016f-109">Ein Zeiger auf das -Objekt, das die [**IDockingWindow-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) implementiert, für die der Monitor geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d016f-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="d016f-110">*hMonNeu* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d016f-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d016f-111">Typ: **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="d016f-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="d016f-112">Ein Handle für den Monitor, der den vorhandenen Standardmonitor ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d016f-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d016f-113">*phMonOld* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d016f-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d016f-114">Typ: **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="d016f-114">Type: **HMONITOR\***</span></span>

<span data-ttu-id="d016f-115">Enthält nach der Rückgabe dieser Funktion einen Zeiger auf das Handle des vorherigen Standardmonitors.</span><span class="sxs-lookup"><span data-stu-id="d016f-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d016f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d016f-116">Return value</span></span>

<span data-ttu-id="d016f-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d016f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d016f-118">Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d016f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d016f-119">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d016f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d016f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d016f-120">Requirements</span></span>



| <span data-ttu-id="d016f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d016f-121">Requirement</span></span> | <span data-ttu-id="d016f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d016f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="d016f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d016f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d016f-124">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d016f-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d016f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d016f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d016f-126">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d016f-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
