---
title: D3DX11UnsetAllDeviceObjects-Funktion (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie die Verknüpfung id3d11devicecontext aus clearstate-Methode verwenden, anstatt diese Funktion zu verwenden.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- D3DX11UnsetAllDeviceObjects-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355337"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a><span data-ttu-id="1beab-105">D3DX11UnsetAllDeviceObjects-Funktion</span><span class="sxs-lookup"><span data-stu-id="1beab-105">D3DX11UnsetAllDeviceObjects function</span></span>

> [!Note]  
> <span data-ttu-id="1beab-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1beab-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="1beab-107">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [**Verknüpfung id3d11devicecontext aus:: clearstate**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) -Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1beab-107">Instead of using this function, we recommend that you use the [**ID3D11DeviceContext::ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) method.</span></span>

 

<span data-ttu-id="1beab-108">Entfernt alle Ressourcen vom Gerät, indem die Zeiger auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1beab-108">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="1beab-109">Dies sollte beim Herunterfahren der Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1beab-109">This should be called during shutdown of your application.</span></span> <span data-ttu-id="1beab-110">Dadurch wird sichergestellt, dass alle Ressourcen freigegeben werden, die nicht an das Gerät gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="1beab-110">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1beab-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1beab-111">Syntax</span></span>


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="1beab-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1beab-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1beab-113">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1beab-113">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1beab-114">Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="1beab-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="1beab-115">Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1beab-115">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1beab-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1beab-116">Return value</span></span>

<span data-ttu-id="1beab-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1beab-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1beab-118">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="1beab-118">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1beab-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1beab-119">Requirements</span></span>



| <span data-ttu-id="1beab-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1beab-120">Requirement</span></span> | <span data-ttu-id="1beab-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1beab-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1beab-122">Header</span><span class="sxs-lookup"><span data-stu-id="1beab-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1beab-123"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1beab-123"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="1beab-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1beab-124">Library</span></span><br/> | <dl> <span data-ttu-id="1beab-125"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1beab-125"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1beab-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1beab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1beab-127">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1beab-127">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





