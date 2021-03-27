---
description: Ruft den aktuellen Standard Monitor ab.
title: 'Imultimonitordockingsite:: getmonitor-Methode'
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
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994943"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="dad7c-103">Imultimonitordockingsite:: getmonitor-Methode</span><span class="sxs-lookup"><span data-stu-id="dad7c-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="dad7c-104">Ruft den aktuellen Standard Monitor ab.</span><span class="sxs-lookup"><span data-stu-id="dad7c-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dad7c-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="dad7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dad7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad7c-107">*punksrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dad7c-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad7c-108">Typ: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="dad7c-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="dad7c-109">Ein Zeiger auf das Objekt, das die [_ *idockingwindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) -Schnittstelle implementiert, für die der Monitor angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="dad7c-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="dad7c-110">*phmon* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dad7c-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad7c-111">Geben Sie Folgendes ein: \**Hmonitor \** _</span><span class="sxs-lookup"><span data-stu-id="dad7c-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="dad7c-112">Wenn die Funktion zurückgegeben wird, enthält Sie einen Zeiger auf das Handle des Standard Monitors.</span><span class="sxs-lookup"><span data-stu-id="dad7c-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad7c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dad7c-113">Return value</span></span>

<span data-ttu-id="dad7c-114">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dad7c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dad7c-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="dad7c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dad7c-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dad7c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad7c-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dad7c-117">Requirements</span></span>



| <span data-ttu-id="dad7c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dad7c-118">Requirement</span></span> | <span data-ttu-id="dad7c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="dad7c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="dad7c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dad7c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dad7c-121">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dad7c-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dad7c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dad7c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dad7c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dad7c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
