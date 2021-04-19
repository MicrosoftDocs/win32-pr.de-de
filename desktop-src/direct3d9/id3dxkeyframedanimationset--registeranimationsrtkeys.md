---
description: Registrieren der schlüsselrahmen Daten für die Skalierung, Drehung und Übersetzung (SRT) für eine Animation.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'ID3DXKeyframedAnimationSet:: registeranimationsrtkeys-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351985"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a><span data-ttu-id="78fda-103">ID3DXKeyframedAnimationSet:: registeranimationsrtkeys-Methode</span><span class="sxs-lookup"><span data-stu-id="78fda-103">ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys method</span></span>

<span data-ttu-id="78fda-104">Registrieren der schlüsselrahmen Daten für die Skalierung, Drehung und Übersetzung (SRT) für eine Animation.</span><span class="sxs-lookup"><span data-stu-id="78fda-104">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="78fda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78fda-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a><span data-ttu-id="78fda-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78fda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78fda-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78fda-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fda-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78fda-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78fda-109">Zeiger auf den Namen der Animation.</span><span class="sxs-lookup"><span data-stu-id="78fda-109">Pointer to the animation name.</span></span>

</dd> <dt>

<span data-ttu-id="78fda-110">*Numscalekeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78fda-110">*NumScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fda-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78fda-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78fda-112">Anzahl der Skalierungs Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="78fda-112">Number of scale keys.</span></span>

</dd> <dt>

<span data-ttu-id="78fda-113">*Numrotationkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78fda-113">*NumRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fda-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78fda-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78fda-115">Anzahl von Rotations Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="78fda-115">Number of rotation keys.</span></span>

</dd> <dt>

<span data-ttu-id="78fda-116">*Numtranslationkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78fda-116">*NumTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fda-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78fda-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78fda-118">Anzahl von Übersetzungs Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="78fda-118">Number of translation keys.</span></span>

</dd> <dt>

<span data-ttu-id="78fda-119">*pscalekeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78fda-119">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fda-120">Typ: **Konstanten [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="78fda-120">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="78fda-121">Adresse eines Zeigers auf ein vom Benutzer zugeordneter [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) Vektoren, das von der Methode mit Skalierungs Daten gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="78fda-121">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with scale data.</span></span>

</dd> <dt>

<span data-ttu-id="78fda-122">" *protationkeys* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="78fda-122">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fda-123">Typ: **Konstanten [**LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="78fda-123">Type: **const [**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)\***</span></span>

<span data-ttu-id="78fda-124">Adresse eines Zeigers auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) -Quaternionen, die die Methode mit den Rotationsdaten füllt.</span><span class="sxs-lookup"><span data-stu-id="78fda-124">Address of a pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method fills with rotation data.</span></span>

</dd> <dt>

<span data-ttu-id="78fda-125">*ptranslationkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78fda-125">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fda-126">Typ: **Konstanten [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="78fda-126">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="78fda-127">Adresse eines Zeigers auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) Vektoren, das die Methode mit Übersetzungs Daten füllt.</span><span class="sxs-lookup"><span data-stu-id="78fda-127">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with translation data.</span></span>

</dd> <dt>

<span data-ttu-id="78fda-128">*panimationindex* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="78fda-128">*pAnimationIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78fda-129">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78fda-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78fda-130">Gibt den Animations Index zurück.</span><span class="sxs-lookup"><span data-stu-id="78fda-130">Returns the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78fda-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78fda-131">Return value</span></span>

<span data-ttu-id="78fda-132">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78fda-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78fda-133">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78fda-133">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="78fda-134">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="78fda-134">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="78fda-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78fda-135">Requirements</span></span>



| <span data-ttu-id="78fda-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78fda-136">Requirement</span></span> | <span data-ttu-id="78fda-137">Wert</span><span class="sxs-lookup"><span data-stu-id="78fda-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78fda-138">Header</span><span class="sxs-lookup"><span data-stu-id="78fda-138">Header</span></span><br/>  | <dl> <span data-ttu-id="78fda-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="78fda-139"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="78fda-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78fda-140">Library</span></span><br/> | <dl> <span data-ttu-id="78fda-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78fda-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78fda-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78fda-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78fda-143">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="78fda-143">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="78fda-144">**ID3DXKeyframedAnimationSet:: getnumscalekeys**</span><span class="sxs-lookup"><span data-stu-id="78fda-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[<span data-ttu-id="78fda-145">**ID3DXKeyframedAnimationSet:: getnumrotationkeys**</span><span class="sxs-lookup"><span data-stu-id="78fda-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[<span data-ttu-id="78fda-146">**ID3DXKeyframedAnimationSet:: getnumtranslationkeys**</span><span class="sxs-lookup"><span data-stu-id="78fda-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
