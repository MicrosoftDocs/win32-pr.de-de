---
description: Entfernt alle Ressourcen vom Gerät, indem die Zeiger auf NULL festgelegt werden. Dies sollte beim Herunterfahren der Anwendung aufgerufen werden. Dadurch wird sichergestellt, dass alle Ressourcen freigegeben werden, die nicht an das Gerät gebunden sind.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: D3DX10UnsetAllDeviceObjects-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355193"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a><span data-ttu-id="1af04-105">D3DX10UnsetAllDeviceObjects-Funktion</span><span class="sxs-lookup"><span data-stu-id="1af04-105">D3DX10UnsetAllDeviceObjects function</span></span>

<span data-ttu-id="1af04-106">Entfernt alle Ressourcen vom Gerät, indem die Zeiger auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1af04-106">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="1af04-107">Dies sollte beim Herunterfahren der Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1af04-107">This should be called during shutdown of your application.</span></span> <span data-ttu-id="1af04-108">Dadurch wird sichergestellt, dass alle Ressourcen freigegeben werden, die nicht an das Gerät gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="1af04-108">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af04-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1af04-109">Syntax</span></span>


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="1af04-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1af04-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af04-111">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1af04-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1af04-112">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="1af04-112">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="1af04-113">Zeiger auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="1af04-113">Pointer to the device.</span></span> <span data-ttu-id="1af04-114">Siehe [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span><span class="sxs-lookup"><span data-stu-id="1af04-114">See [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af04-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1af04-115">Return value</span></span>

<span data-ttu-id="1af04-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1af04-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1af04-117">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="1af04-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1af04-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1af04-118">Requirements</span></span>



| <span data-ttu-id="1af04-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1af04-119">Requirement</span></span> | <span data-ttu-id="1af04-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1af04-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1af04-121">Header</span><span class="sxs-lookup"><span data-stu-id="1af04-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1af04-122"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af04-122"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="1af04-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1af04-123">Library</span></span><br/> | <dl> <span data-ttu-id="1af04-124"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1af04-124"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1af04-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1af04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af04-126">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="1af04-126">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




