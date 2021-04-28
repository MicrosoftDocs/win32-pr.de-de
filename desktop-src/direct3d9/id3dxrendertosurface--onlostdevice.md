---
description: 'ID3DXRenderToSurface::OnLostDevice-Methode: Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.'
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: ID3DXRenderToSurface::OnLostDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 772b678dc4260954c2e03c13d7259565cd896bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093113"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a><span data-ttu-id="7fac4-104">ID3DXRenderToSurface::OnLostDevice-Methode</span><span class="sxs-lookup"><span data-stu-id="7fac4-104">ID3DXRenderToSurface::OnLostDevice method</span></span>

<span data-ttu-id="7fac4-105">Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7fac4-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="7fac4-106">Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.</span><span class="sxs-lookup"><span data-stu-id="7fac4-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fac4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fac4-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="7fac4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fac4-108">Parameters</span></span>

<span data-ttu-id="7fac4-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7fac4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fac4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fac4-110">Return value</span></span>

<span data-ttu-id="7fac4-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7fac4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7fac4-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7fac4-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7fac4-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="7fac4-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fac4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fac4-114">Remarks</span></span>

<span data-ttu-id="7fac4-115">Diese Methode sollte immer dann aufgerufen werden, wenn das Gerät verloren geht oder bevor der Benutzer [**IDirect3DDevice9::Reset aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)</span><span class="sxs-lookup"><span data-stu-id="7fac4-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset).</span></span> <span data-ttu-id="7fac4-116">Selbst wenn das Gerät nicht tatsächlich verloren gegangen ist, ist ID3DXRenderToSurface::OnLostDevice für die Freigabe von Zustandsblocks und anderen Ressourcen verantwortlich, die möglicherweise freigegeben werden müssen, bevor das Gerät zurück gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7fac4-116">Even if the device was not actually lost, ID3DXRenderToSurface::OnLostDevice is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="7fac4-117">Daher kann das Schriftartobjekt vor dem Aufruf von **IDirect3DDevice9::Reset** und id3DXRenderToSurface::OnResetDevice nicht erneut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fac4-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then ID3DXRenderToSurface::OnResetDevice.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fac4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fac4-118">Requirements</span></span>



| <span data-ttu-id="7fac4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fac4-119">Requirement</span></span> | <span data-ttu-id="7fac4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7fac4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fac4-121">Header</span><span class="sxs-lookup"><span data-stu-id="7fac4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7fac4-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="7fac4-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7fac4-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7fac4-123">Library</span></span><br/> | <dl> <span data-ttu-id="7fac4-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fac4-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7fac4-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7fac4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fac4-126">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="7fac4-126">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
