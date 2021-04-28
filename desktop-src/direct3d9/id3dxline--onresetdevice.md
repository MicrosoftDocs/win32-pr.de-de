---
description: 'ID3DXLine::OnResetDevice-Methode: Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.'
ms.assetid: beca7a51-e799-4e03-81a3-218552231428
title: ID3DXLine::OnResetDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7e1275e7a7ec894601dc67503e25e1fa82545f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093658"
---
# <a name="id3dxlineonresetdevice-method"></a><span data-ttu-id="68b26-103">ID3DXLine::OnResetDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="68b26-103">ID3DXLine::OnResetDevice method</span></span>

<span data-ttu-id="68b26-104">Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.</span><span class="sxs-lookup"><span data-stu-id="68b26-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68b26-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="68b26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68b26-106">Parameters</span></span>

<span data-ttu-id="68b26-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="68b26-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68b26-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68b26-108">Return value</span></span>

<span data-ttu-id="68b26-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68b26-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68b26-110">Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="68b26-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="68b26-111">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="68b26-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b26-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68b26-112">Remarks</span></span>

<span data-ttu-id="68b26-113">**ID3DXLine::OnResetDevice** sollte jedes Mal aufgerufen werden, wenn das Gerät zurückgesetzt wird (mit [**IDirect3DDevice9::Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)bevor andere Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="68b26-113">**ID3DXLine::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="68b26-114">Dies ist ein guter Ort zum erneuten Abrufen von Videospeicherressourcen und Erfassen von Zustandsblöcken.</span><span class="sxs-lookup"><span data-stu-id="68b26-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b26-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68b26-115">Requirements</span></span>



| <span data-ttu-id="68b26-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68b26-116">Requirement</span></span> | <span data-ttu-id="68b26-117">Wert</span><span class="sxs-lookup"><span data-stu-id="68b26-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b26-118">Header</span><span class="sxs-lookup"><span data-stu-id="68b26-118">Header</span></span><br/>  | <dl> <span data-ttu-id="68b26-119"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="68b26-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="68b26-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68b26-120">Library</span></span><br/> | <dl> <span data-ttu-id="68b26-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="68b26-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68b26-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="68b26-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b26-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="68b26-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
