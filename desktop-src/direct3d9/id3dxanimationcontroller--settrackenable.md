---
description: Aktiviert oder deaktiviert eine Spur im Animations Controller.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'ID3DXAnimationController:: settrackenable-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050908"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a><span data-ttu-id="2814c-103">ID3DXAnimationController:: settrackenable-Methode</span><span class="sxs-lookup"><span data-stu-id="2814c-103">ID3DXAnimationController::SetTrackEnable method</span></span>

<span data-ttu-id="2814c-104">Aktiviert oder deaktiviert eine Spur im Animations Controller.</span><span class="sxs-lookup"><span data-stu-id="2814c-104">Enables or disables a track in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="2814c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2814c-105">Syntax</span></span>


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="2814c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2814c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2814c-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2814c-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2814c-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2814c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2814c-109">Der Bezeichner des Titels, der gemischt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2814c-109">Identifier of the track to be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="2814c-110">*Aktivieren* \[ von in\]</span><span class="sxs-lookup"><span data-stu-id="2814c-110">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2814c-111">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2814c-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2814c-112">Aktivieren Sie den Wert.</span><span class="sxs-lookup"><span data-stu-id="2814c-112">Enable value.</span></span> <span data-ttu-id="2814c-113">Legen Sie diese Einstellung auf " **true** " fest, um diese Spur im Controller zu aktivieren, oder auf " **false** ", um eine Vermischung zu verhindern</span><span class="sxs-lookup"><span data-stu-id="2814c-113">Set to **TRUE** to enable this track in the controller, or to **FALSE** to prevent it from being mixed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2814c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2814c-114">Return value</span></span>

<span data-ttu-id="2814c-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2814c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2814c-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2814c-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2814c-117">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="2814c-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2814c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2814c-118">Remarks</span></span>

<span data-ttu-id="2814c-119">Das Enable-Flag muss auf " **true**" festgelegt werden, um eine Spur mit anderen Spuren zu mischen.</span><span class="sxs-lookup"><span data-stu-id="2814c-119">To mix a track with other tracks, the Enable flag must be set to **TRUE**.</span></span> <span data-ttu-id="2814c-120">Umgekehrt verhindert das Festlegen des Flags auf **false** , dass der Track nicht mit anderen Spuren gemischt wird.</span><span class="sxs-lookup"><span data-stu-id="2814c-120">Conversely, setting the flag to **FALSE** will prevent the track from being mixed with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="2814c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2814c-121">Requirements</span></span>



| <span data-ttu-id="2814c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2814c-122">Requirement</span></span> | <span data-ttu-id="2814c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2814c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2814c-124">Header</span><span class="sxs-lookup"><span data-stu-id="2814c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2814c-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2814c-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2814c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2814c-126">Library</span></span><br/> | <dl> <span data-ttu-id="2814c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2814c-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2814c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2814c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2814c-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2814c-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
