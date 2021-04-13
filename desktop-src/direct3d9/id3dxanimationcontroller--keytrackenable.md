---
description: Legt einen Ereignis Schlüssel fest, der einen Animations Titel aktiviert oder deaktiviert.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'ID3DXAnimationController:: keytrackenable-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354256"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a><span data-ttu-id="4e75c-103">ID3DXAnimationController:: keytrackenable-Methode</span><span class="sxs-lookup"><span data-stu-id="4e75c-103">ID3DXAnimationController::KeyTrackEnable method</span></span>

<span data-ttu-id="4e75c-104">Legt einen Ereignis Schlüssel fest, der einen Animations Titel aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4e75c-104">Sets an event key that enables or disables an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e75c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e75c-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="4e75c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e75c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e75c-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e75c-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e75c-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e75c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e75c-109">Der Bezeichner des zu ändernden Animations Titels.</span><span class="sxs-lookup"><span data-stu-id="4e75c-109">Identifier of the animation track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="4e75c-110">Kann nicht angezeigt werden  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e75c-110">*NewEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e75c-111">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e75c-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e75c-112">Flag aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4e75c-112">Enable flag.</span></span> <span data-ttu-id="4e75c-113">Legen Sie diese Einstellung auf " **true** " fest, um den Animations Titel zu aktivieren, oder auf " **false** ", um die</span><span class="sxs-lookup"><span data-stu-id="4e75c-113">Set this to **TRUE** to enable the animation track, or to **FALSE** to disable the track.</span></span>

</dd> <dt>

<span data-ttu-id="4e75c-114">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e75c-114">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e75c-115">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e75c-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e75c-116">Globaler Zeit Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="4e75c-116">Global time key.</span></span> <span data-ttu-id="4e75c-117">Gibt die globale Zeit an, zu der die Änderung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="4e75c-117">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e75c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e75c-118">Return value</span></span>

<span data-ttu-id="4e75c-119">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="4e75c-119">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="4e75c-120">Ereignis Handle für das Priority Blend-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4e75c-120">Event handle to the priority blend event.</span></span> <span data-ttu-id="4e75c-121">**Null** wird zurückgegeben, wenn der Titel ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="4e75c-121">**NULL** is returned if Track is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e75c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e75c-122">Requirements</span></span>



| <span data-ttu-id="4e75c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e75c-123">Requirement</span></span> | <span data-ttu-id="4e75c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4e75c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e75c-125">Header</span><span class="sxs-lookup"><span data-stu-id="4e75c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4e75c-126"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e75c-126"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4e75c-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e75c-127">Library</span></span><br/> | <dl> <span data-ttu-id="4e75c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e75c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e75c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e75c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e75c-130">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="4e75c-130">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
