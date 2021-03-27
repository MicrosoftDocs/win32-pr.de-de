---
description: Ändert, welcher Monitor für angedockte Symbolleisten in einem System mit mehreren Monitoren verwendet wird.
title: 'Imultimonitordockingsite:: setmonitor-Methode'
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
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995199"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="90549-103">Imultimonitordockingsite:: setmonitor-Methode</span><span class="sxs-lookup"><span data-stu-id="90549-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="90549-104">Ändert, welcher Monitor für angedockte Symbolleisten in einem System mit mehreren Monitoren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90549-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="90549-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90549-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="90549-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="90549-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90549-107">*punksrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90549-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90549-108">Typ: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="90549-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="90549-109">Ein Zeiger auf das Objekt, das die [_ *idockingwindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) -Schnittstelle implementiert, für die der Monitor geändert wird.</span><span class="sxs-lookup"><span data-stu-id="90549-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="90549-110">*hmonnew* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90549-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90549-111">Typ: **Hmonitor**</span><span class="sxs-lookup"><span data-stu-id="90549-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="90549-112">Ein Handle für den Monitor, der den vorhandenen Standard Monitor ersetzt.</span><span class="sxs-lookup"><span data-stu-id="90549-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="90549-113">*phmonold* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="90549-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90549-114">Geben Sie Folgendes ein: \**Hmonitor \** _</span><span class="sxs-lookup"><span data-stu-id="90549-114">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="90549-115">Diese Funktion gibt einen Zeiger auf das vorherige Standard Monitor Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="90549-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90549-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90549-116">Return value</span></span>

<span data-ttu-id="90549-117">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="90549-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="90549-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="90549-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="90549-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90549-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="90549-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="90549-120">Requirements</span></span>



| <span data-ttu-id="90549-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90549-121">Requirement</span></span> | <span data-ttu-id="90549-122">Wert</span><span class="sxs-lookup"><span data-stu-id="90549-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="90549-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90549-123">Minimum supported client</span></span><br/> | <span data-ttu-id="90549-124">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90549-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90549-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90549-125">Minimum supported server</span></span><br/> | <span data-ttu-id="90549-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90549-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
