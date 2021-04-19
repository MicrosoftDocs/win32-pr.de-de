---
description: 'Die Anwendung implementiert diese Methode. Diese Methode wird aufgerufen, wenn ein Rückruf für einen Animations Satz in einer der-Spuren während eines Aufrufs von ID3DXAnimationController:: AdvanceTime auftritt.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'ID3DXAnimationCallbackHandler:: Lenker Callback-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360235"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a><span data-ttu-id="a92b8-104">ID3DXAnimationCallbackHandler:: Lenker Callback-Methode</span><span class="sxs-lookup"><span data-stu-id="a92b8-104">ID3DXAnimationCallbackHandler::HandleCallback method</span></span>

<span data-ttu-id="a92b8-105">Die Anwendung implementiert diese Methode.</span><span class="sxs-lookup"><span data-stu-id="a92b8-105">The application implements this method.</span></span> <span data-ttu-id="a92b8-106">Diese Methode wird aufgerufen, wenn ein Rückruf für einen Animations Satz in einer der-Spuren während eines Aufrufs von [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md)auftritt.</span><span class="sxs-lookup"><span data-stu-id="a92b8-106">This method is called when a callback occurs for an animation set in one of the tracks during a call to [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a92b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a92b8-107">Syntax</span></span>


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="a92b8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a92b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92b8-109">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a92b8-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92b8-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a92b8-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a92b8-111">Der Bezeichner der Spur, auf der der Rückruf auftritt.</span><span class="sxs-lookup"><span data-stu-id="a92b8-111">Identifier of the track on which the callback occurs.</span></span>

</dd> <dt>

<span data-ttu-id="a92b8-112">*pcallbackdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a92b8-112">*pCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92b8-113">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a92b8-113">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a92b8-114">Zeiger auf Benutzer eigene Rückruf Daten.</span><span class="sxs-lookup"><span data-stu-id="a92b8-114">Pointer to user-owned callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a92b8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a92b8-115">Return value</span></span>

<span data-ttu-id="a92b8-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a92b8-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a92b8-117">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="a92b8-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="a92b8-118">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="a92b8-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="a92b8-119">Andernfalls programmieren Sie die-Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a92b8-119">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a92b8-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a92b8-120">Requirements</span></span>



| <span data-ttu-id="a92b8-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a92b8-121">Requirement</span></span> | <span data-ttu-id="a92b8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a92b8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a92b8-123">Header</span><span class="sxs-lookup"><span data-stu-id="a92b8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a92b8-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a92b8-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a92b8-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a92b8-125">Library</span></span><br/> | <dl> <span data-ttu-id="a92b8-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a92b8-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a92b8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a92b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92b8-128">ID3DXAnimationCallbackHandler</span><span class="sxs-lookup"><span data-stu-id="a92b8-128">ID3DXAnimationCallbackHandler</span></span>](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
