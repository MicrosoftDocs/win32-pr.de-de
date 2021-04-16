---
description: Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: 'ID3DXFont:: OnResetDevice-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6e65001f484ed7d7a984ed1f9463b996056e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394173"
---
# <a name="id3dxfontonresetdevice-method"></a><span data-ttu-id="e29c1-103">ID3DXFont:: OnResetDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="e29c1-103">ID3DXFont::OnResetDevice method</span></span>

<span data-ttu-id="e29c1-104">Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e29c1-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e29c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e29c1-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="e29c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e29c1-106">Parameters</span></span>

<span data-ttu-id="e29c1-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e29c1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e29c1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e29c1-108">Return value</span></span>

<span data-ttu-id="e29c1-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e29c1-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e29c1-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e29c1-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e29c1-111">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="e29c1-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e29c1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e29c1-112">Remarks</span></span>

<span data-ttu-id="e29c1-113">**OnResetDevice** sollte jedes Mal aufgerufen werden, wenn das Gerät zurückgesetzt wird (mithilfe von [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), bevor andere Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e29c1-113">**OnResetDevice** should be called each time the device is reset (using [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="e29c1-114">Dies ist ein guter Ort zum erneuten Abrufen von Video-Memory-Ressourcen und zum Erfassen von Zustands Blöcken.</span><span class="sxs-lookup"><span data-stu-id="e29c1-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="e29c1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e29c1-115">Requirements</span></span>



| <span data-ttu-id="e29c1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e29c1-116">Requirement</span></span> | <span data-ttu-id="e29c1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e29c1-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e29c1-118">Header</span><span class="sxs-lookup"><span data-stu-id="e29c1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e29c1-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e29c1-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e29c1-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e29c1-120">Library</span></span><br/> | <dl> <span data-ttu-id="e29c1-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e29c1-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e29c1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e29c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e29c1-123">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="e29c1-123">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
