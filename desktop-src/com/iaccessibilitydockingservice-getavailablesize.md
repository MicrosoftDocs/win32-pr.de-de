---
title: Iaccessibilitydockingservice getavailablesize-Methode
description: Ruft die Dimensionen ab, die zum Andocken eines Barrierefreiheits Fensters eines Monitors verfügbar sind.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Getavailablesize-Methode com
- Getavailablesize-Methode com, iaccessibilitydockingservice-Schnittstelle
- Iaccessibilitydockingservice-Schnittstelle com, getavailablesize-Methode
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037930"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a><span data-ttu-id="6a158-106">Iaccessibilitydockingservice:: getavailablesize-Methode</span><span class="sxs-lookup"><span data-stu-id="6a158-106">IAccessibilityDockingService::GetAvailableSize method</span></span>

<span data-ttu-id="6a158-107">Ruft die Dimensionen ab, die zum Andocken eines Barrierefreiheits Fensters eines Monitors verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6a158-107">Gets the dimensions available for docking an accessibility window on a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a158-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a158-108">Syntax</span></span>


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a><span data-ttu-id="6a158-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a158-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a158-110">*Hmonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a158-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a158-111">Gibt den Monitor an, für den die verfügbare Docking Größe abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6a158-111">Specifies the monitor for which the available docking size will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="6a158-112">*pumaxheight* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a158-112">*puMaxHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a158-113">Legen Sie bei Erfolg auf die maximale Höhe fest, die für das Andocken auf dem angegebenen *Hmonitor* in Pixel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6a158-113">On success, set to the maximum height available for docking on the specified *hMonitor*, in pixels.</span></span>

<span data-ttu-id="6a158-114">Bei einem Fehler wird auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6a158-114">On failure, set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6a158-115">*pufixedwidth* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a158-115">*puFixedWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a158-116">Legen Sie bei Erfolg auf die festgelegte Breite fest, die für das Andocken auf dem angegebenen *Hmonitor* in Pixel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6a158-116">On success, set to the fixed width available for docking on the specified *hMonitor*, in pixels.</span></span> <span data-ttu-id="6a158-117">Jedes Fenster, das an diesen *Hmonitor* angedockt ist, wird auf diese Breite vergrößert.</span><span class="sxs-lookup"><span data-stu-id="6a158-117">Any window docked to this *hMonitor* will be sized to this width.</span></span>

<span data-ttu-id="6a158-118">Bei einem Fehler wird auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6a158-118">On failure, set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a158-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a158-119">Return value</span></span>



| <span data-ttu-id="6a158-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6a158-120">Return code</span></span>                                                                                                                          | <span data-ttu-id="6a158-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a158-121">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a158-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6a158-122"><dt>**S\_OK**</dt></span></span> </dl>                                                 | <span data-ttu-id="6a158-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6a158-123">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="6a158-124"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ ungültiges \_ Monitor \_ handle)**</dt></span><span class="sxs-lookup"><span data-stu-id="6a158-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_MONITOR\_HANDLE)**</dt></span></span> </dl> | <span data-ttu-id="6a158-125">Der vom Monitor handle angegebene Monitor unterstützt das Andocken nicht.</span><span class="sxs-lookup"><span data-stu-id="6a158-125">The monitor specified by the monitor handle does not support docking.</span></span><br/> |



 

<span data-ttu-id="6a158-126">Wenn entweder *pumaxheight* oder *pufixedwidth* NULL ist, tritt eine Zugriffsverletzung auf.</span><span class="sxs-lookup"><span data-stu-id="6a158-126">If either *puMaxHeight* or *puFixedWidth* are null, an access violation will occur.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a158-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a158-127">Remarks</span></span>

<span data-ttu-id="6a158-128">Barrierefreiheits Fenster können nur an einen Monitor angedockt werden, der mindestens 768 vertikale Bildschirm Pixel aufweist.</span><span class="sxs-lookup"><span data-stu-id="6a158-128">Accessibility windows can only be docked to a monitor that has at least 768 vertical screen pixels.</span></span> <span data-ttu-id="6a158-129">Diese API lässt nicht zu, dass solche Fenster mit einer Höhe angedockt werden, die dazu führt, dass Windows Store-Apps weniger als 768 vertikale Bildschirm Pixel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6a158-129">This API will not allow such windows to be docked with a height that would cause Windows Store apps to have less than 768 vertical screen pixels.</span></span>

## <a name="examples"></a><span data-ttu-id="6a158-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a158-130">Examples</span></span>


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a><span data-ttu-id="6a158-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6a158-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a158-132">**Iaccessibilitydockingservice**</span><span class="sxs-lookup"><span data-stu-id="6a158-132">**IAccessibilityDockingService**</span></span>](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





