---
description: Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer und fügt die Daten einem IDirect3DTexture9-Objekt hinzu.
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'ID3DXPRTCompBuffer:: extracttexture-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6a2200c680c19019375a5e33d2d8b675992dc38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050882"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a><span data-ttu-id="a374b-103">ID3DXPRTCompBuffer:: extracttexture-Methode</span><span class="sxs-lookup"><span data-stu-id="a374b-103">ID3DXPRTCompBuffer::ExtractTexture method</span></span>

<span data-ttu-id="a374b-104">Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Datenpuffer und fügt die Daten einem [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a374b-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a374b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a374b-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="a374b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a374b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a374b-107">*Startpca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a374b-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a374b-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a374b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a374b-109">Startwert des Puffer Koeffizienten, von dem Textur Daten extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a374b-109">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="a374b-110">*Numpca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a374b-110">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a374b-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a374b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a374b-112">Anzahl der PCA-Koeffizienten, die aus dem Puffer extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a374b-112">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a374b-113">*ptexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a374b-113">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a374b-114">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="a374b-114">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="a374b-115">Zeiger auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Textur Objekt, in dem die PCA-Koeffizienten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a374b-115">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a374b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a374b-116">Return value</span></span>

<span data-ttu-id="a374b-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a374b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a374b-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a374b-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a374b-119">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a374b-119">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a374b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a374b-120">Requirements</span></span>



| <span data-ttu-id="a374b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a374b-121">Requirement</span></span> | <span data-ttu-id="a374b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a374b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a374b-123">Header</span><span class="sxs-lookup"><span data-stu-id="a374b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a374b-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a374b-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a374b-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a374b-125">Library</span></span><br/> | <dl> <span data-ttu-id="a374b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a374b-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a374b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a374b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a374b-128">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="a374b-128">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
