---
description: Legen Sie einen zusammenhängenden Bereich von shaderkonstanten mit einer Speicher Kopie fest.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'ID3DXEffect:: strawvalue-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354997"
---
# <a name="id3dxeffectsetrawvalue-method"></a><span data-ttu-id="59e09-103">ID3DXEffect:: strawvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="59e09-103">ID3DXEffect::SetRawValue method</span></span>

<span data-ttu-id="59e09-104">Legen Sie einen zusammenhängenden Bereich von shaderkonstanten mit einer Speicher Kopie fest.</span><span class="sxs-lookup"><span data-stu-id="59e09-104">Set a contiguous range of shader constants with a memory copy.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59e09-105">Syntax</span></span>


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="59e09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59e09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e09-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59e09-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e09-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="59e09-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="59e09-109">Handle für den festzulegenden Wert oder den Namen des Werts, der als Zeichenfolge übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="59e09-109">Handle to the value to set, or the name of the value passed in as a string.</span></span> <span data-ttu-id="59e09-110">Das Übergeben eines Handles ist effizienter.</span><span class="sxs-lookup"><span data-stu-id="59e09-110">Passing in a handle is more efficient.</span></span> <span data-ttu-id="59e09-111">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="59e09-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="59e09-112">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59e09-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e09-113">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="59e09-113">Type: **void\***</span></span>

<span data-ttu-id="59e09-114">Zeiger auf einen Puffer, der die Daten enthält, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="59e09-114">Pointer to a buffer containing the data to be set.</span></span> <span data-ttu-id="59e09-115">"Strawvalue" prüft, ob ein gültiger Arbeitsspeicher vorhanden ist, überprüft jedoch keine gültigen Daten.</span><span class="sxs-lookup"><span data-stu-id="59e09-115">SetRawValue checks for valid memory, but does not do any checking for valid data.</span></span>

</dd> <dt>

<span data-ttu-id="59e09-116">*Offestinbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59e09-116">*OffsetInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e09-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59e09-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59e09-118">Anzahl von Bytes zwischen dem Anfang der Wirkungs Daten und dem Anfang der Effekt Konstanten, die festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="59e09-118">Number of bytes between the beginning of the effect data and the beginning of the effect constants you are going to set.</span></span>

</dd> <dt>

<span data-ttu-id="59e09-119">*Bytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59e09-119">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e09-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59e09-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59e09-121">Die Größe des festzulegenden Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="59e09-121">The size of the buffer to be set, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e09-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59e09-122">Return value</span></span>

<span data-ttu-id="59e09-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59e09-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59e09-124">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59e09-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59e09-125">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: E \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="59e09-125">If the method fails, the return value can be one of the following:E\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e09-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59e09-126">Remarks</span></span>

<span data-ttu-id="59e09-127">Setrawvalue ist eine sehr schnelle Möglichkeit zum Festlegen von Effekt Konstanten, da eine Speicher Kopie ohne Validierung oder Datenkonvertierung (z. b. die Konvertierung einer Zeilen hauptmatrix in eine Spalten hauptmatrix) durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59e09-127">SetRawValue is a very fast way to set effect constants since it performs a memory copy without performing validation or any data conversion (like converting a row-major matrix to a column-major matrix).</span></span> <span data-ttu-id="59e09-128">Verwenden Sie setrawvalue, um eine Reihe zusammenhängender Wirkungs Konstanten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="59e09-128">Use SetRawValue to set a series of contiguous effect constants.</span></span> <span data-ttu-id="59e09-129">Beispielsweise können Sie ein Array von 20 Matrizen mit 20 Aufrufen von [**ID3DXBaseEffect:: setMatrix**](id3dxbaseeffect--setmatrix.md) oder mithilfe eines einzelnen setrawvalue festlegen.</span><span class="sxs-lookup"><span data-stu-id="59e09-129">For instance, you could set an array of twenty matrices with 20 calls to [**ID3DXBaseEffect::SetMatrix**](id3dxbaseeffect--setmatrix.md) or by using a single SetRawValue.</span></span>

<span data-ttu-id="59e09-130">Alle Werte werden als "matrix4x4s" oder "float4s" erwartet, und es wird erwartet, dass alle Matrizen in der Spalten Hauptreihen Folge sind.</span><span class="sxs-lookup"><span data-stu-id="59e09-130">All values are expected to be either matrix4x4s or float4s and all matrices are expected to be in column-major order.</span></span> <span data-ttu-id="59e09-131">Int-oder float-Werte werden in einen float4-Wert umgewandelt. Daher wird dringend empfohlen, dass Sie "strawvalue" nur mit "float4" oder "matrix4x4" verwenden.</span><span class="sxs-lookup"><span data-stu-id="59e09-131">Int or float values are cast into a float4; therefore, it is highly recommended that you use SetRawValue with only float4 or matrix4x4 data.</span></span>

## <a name="requirements"></a><span data-ttu-id="59e09-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59e09-132">Requirements</span></span>



| <span data-ttu-id="59e09-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59e09-133">Requirement</span></span> | <span data-ttu-id="59e09-134">Wert</span><span class="sxs-lookup"><span data-stu-id="59e09-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e09-135">Header</span><span class="sxs-lookup"><span data-stu-id="59e09-135">Header</span></span><br/>  | <dl> <span data-ttu-id="59e09-136"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="59e09-136"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="59e09-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59e09-137">Library</span></span><br/> | <dl> <span data-ttu-id="59e09-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59e09-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="59e09-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59e09-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e09-140">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="59e09-140">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
