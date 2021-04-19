---
description: Legt einen Zeiger auf eine optionale Rückruffunktion fest, die den Prozentsatz der abzurufenden sphärischen (SH) Berechnungen berechnet und dem Aufrufer die Möglichkeit gibt, den Simulator abzubrechen.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'ID3DXPRTEngine:: SetCallback-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350698"
---
# <a name="id3dxprtenginesetcallback-method"></a><span data-ttu-id="d06c8-103">ID3DXPRTEngine:: SetCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="d06c8-103">ID3DXPRTEngine::SetCallBack method</span></span>

<span data-ttu-id="d06c8-104">Legt einen Zeiger auf eine optionale Rückruffunktion fest, die den Prozentsatz der abzurufenden sphärischen (SH) Berechnungen berechnet und dem Aufrufer die Möglichkeit gibt, den Simulator abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="d06c8-104">Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="d06c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d06c8-105">Syntax</span></span>


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="d06c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d06c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d06c8-107">*Platine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d06c8-107">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d06c8-108">Typ: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="d06c8-108">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="d06c8-109">Ein Zeiger auf die [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) -Rückruffunktion, die den Prozentsatz der abgeschlossenen SH-Berechnungen berechnet.</span><span class="sxs-lookup"><span data-stu-id="d06c8-109">Pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that computes the percentage of SH computations completed.</span></span> <span data-ttu-id="d06c8-110">Die Rückruffunktion muss implementiert werden, damit S OK zurückgegeben wird \_ , um den Simulator weiterhin ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="d06c8-110">The callback function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="d06c8-111">Bei jedem anderen Wert wird der Simulator abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d06c8-111">Any other value will abort the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="d06c8-112">*Häufigkeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d06c8-112">*Frequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d06c8-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d06c8-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d06c8-114">Häufigkeit von Rückruf aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d06c8-114">Frequency of callback calls.</span></span> <span data-ttu-id="d06c8-115">Die Umkehrung der Häufigkeit entspricht ungefähr der Häufigkeit, mit der die Rückruffunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d06c8-115">The inverse of Frequency is approximately the number of times the callback function will be called.</span></span>

</dd> <dt>

<span data-ttu-id="d06c8-116">*lpusercontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d06c8-116">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d06c8-117">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d06c8-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d06c8-118">Ein Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d06c8-118">Pointer to a user-defined value which is passed to the callback function.</span></span> <span data-ttu-id="d06c8-119">Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d06c8-119">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d06c8-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d06c8-120">Return value</span></span>

<span data-ttu-id="d06c8-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d06c8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d06c8-122">Der Rückgabewert ist "S \_ OK".</span><span class="sxs-lookup"><span data-stu-id="d06c8-122">The return value is S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d06c8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d06c8-123">Requirements</span></span>



| <span data-ttu-id="d06c8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d06c8-124">Requirement</span></span> | <span data-ttu-id="d06c8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d06c8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d06c8-126">Header</span><span class="sxs-lookup"><span data-stu-id="d06c8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d06c8-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d06c8-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d06c8-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d06c8-128">Library</span></span><br/> | <dl> <span data-ttu-id="d06c8-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d06c8-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d06c8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d06c8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d06c8-131">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="d06c8-131">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
