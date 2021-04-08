---
description: Setzt die globale Animations Zeit auf 0 (null) zurück. Alle ausstehenden Ereignisse behalten ihre ursprünglichen Zeitpläne, aber im neuen Zeitrahmen bei.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'ID3DXAnimationController:: ResetTime-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762210"
---
# <a name="id3dxanimationcontrollerresettime-method"></a><span data-ttu-id="54f22-104">ID3DXAnimationController:: ResetTime-Methode</span><span class="sxs-lookup"><span data-stu-id="54f22-104">ID3DXAnimationController::ResetTime method</span></span>

<span data-ttu-id="54f22-105">Setzt die globale Animations Zeit auf 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="54f22-105">Resets the global animation time to zero.</span></span> <span data-ttu-id="54f22-106">Alle ausstehenden Ereignisse behalten ihre ursprünglichen Zeitpläne, aber im neuen Zeitrahmen bei.</span><span class="sxs-lookup"><span data-stu-id="54f22-106">Any pending events will retain their original schedules, but in the new timeframe.</span></span>

## <a name="syntax"></a><span data-ttu-id="54f22-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="54f22-107">Syntax</span></span>


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a><span data-ttu-id="54f22-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="54f22-108">Parameters</span></span>

<span data-ttu-id="54f22-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="54f22-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54f22-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54f22-110">Return value</span></span>

<span data-ttu-id="54f22-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54f22-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54f22-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54f22-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="54f22-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="54f22-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="54f22-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54f22-114">Remarks</span></span>

<span data-ttu-id="54f22-115">Diese Methode wird normalerweise verwendet, wenn der Wert der globalen Animations Zeit der maximalen Genauigkeit von Double-Speicher entspricht, oder 2 ⁶ ⁴-1.</span><span class="sxs-lookup"><span data-stu-id="54f22-115">This method is typically used when the global animation time value is nearing the maximum precision of DOUBLE storage, or 2⁶⁴ - 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="54f22-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54f22-116">Requirements</span></span>



| <span data-ttu-id="54f22-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54f22-117">Requirement</span></span> | <span data-ttu-id="54f22-118">Wert</span><span class="sxs-lookup"><span data-stu-id="54f22-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54f22-119">Header</span><span class="sxs-lookup"><span data-stu-id="54f22-119">Header</span></span><br/>  | <dl> <span data-ttu-id="54f22-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="54f22-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="54f22-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54f22-121">Library</span></span><br/> | <dl> <span data-ttu-id="54f22-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54f22-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54f22-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54f22-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f22-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="54f22-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




