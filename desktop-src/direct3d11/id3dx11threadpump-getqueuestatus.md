---
title: ID3DX11ThreadPump getqueuestatus-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe ab.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Getqueuestatus-Methode Direct3D 11
- Getqueuestatus-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump-Schnittstelle Direct3D 11, getqueuestatus-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982233"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a><span data-ttu-id="2c9fe-107">ID3DX11ThreadPump:: getqueuestatus-Methode</span><span class="sxs-lookup"><span data-stu-id="2c9fe-107">ID3DX11ThreadPump::GetQueueStatus method</span></span>

> [!Note]  
> <span data-ttu-id="2c9fe-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c9fe-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="2c9fe-109">Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe ab.</span><span class="sxs-lookup"><span data-stu-id="2c9fe-109">Gets the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c9fe-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c9fe-110">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="2c9fe-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c9fe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c9fe-112">*pioqueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c9fe-112">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c9fe-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="2c9fe-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="2c9fe-114">Anzahl der Elemente in der e/a-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2c9fe-114">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="2c9fe-115">*pprocessqueue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c9fe-115">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c9fe-116">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="2c9fe-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="2c9fe-117">Anzahl der Elemente in der Verarbeitungs Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2c9fe-117">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="2c9fe-118">*pdevicequeue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c9fe-118">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c9fe-119">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="2c9fe-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="2c9fe-120">Anzahl der Elemente in der Geräte Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2c9fe-120">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c9fe-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c9fe-121">Return value</span></span>

<span data-ttu-id="2c9fe-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c9fe-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c9fe-123">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="2c9fe-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c9fe-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2c9fe-124">Requirements</span></span>



| <span data-ttu-id="2c9fe-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c9fe-125">Requirement</span></span> | <span data-ttu-id="2c9fe-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2c9fe-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c9fe-127">Header</span><span class="sxs-lookup"><span data-stu-id="2c9fe-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2c9fe-128"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c9fe-128"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="2c9fe-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2c9fe-129">Library</span></span><br/> | <dl> <span data-ttu-id="2c9fe-130"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c9fe-130"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2c9fe-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2c9fe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c9fe-132">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="2c9fe-132">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="2c9fe-133">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2c9fe-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

