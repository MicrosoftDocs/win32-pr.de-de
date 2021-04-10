---
description: Liest die Binärdaten. Veraltet.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'Idirectxfilebinary:: Read-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050904"
---
# <a name="idirectxfilebinaryread-method"></a><span data-ttu-id="66cff-104">Idirectxfilebinary:: Read-Methode</span><span class="sxs-lookup"><span data-stu-id="66cff-104">IDirectXFileBinary::Read method</span></span>

<span data-ttu-id="66cff-105">Liest die Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="66cff-105">Reads the binary data.</span></span> <span data-ttu-id="66cff-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="66cff-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="66cff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="66cff-107">Syntax</span></span>


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="66cff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="66cff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66cff-109">*pvData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="66cff-109">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66cff-110">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66cff-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66cff-111">Zeiger auf den Puffer, der die gelesenen Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="66cff-111">Pointer to the buffer that receives the data that has been read.</span></span>

</dd> <dt>

<span data-ttu-id="66cff-112">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66cff-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66cff-113">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66cff-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66cff-114">Größe des Puffers, auf den pvData zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="66cff-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="66cff-115">*pcbread* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="66cff-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66cff-116">Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66cff-116">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66cff-117">Ein Zeiger auf die Anzahl der tatsächlich gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="66cff-117">Pointer to the number of bytes actually read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66cff-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66cff-118">Return value</span></span>

<span data-ttu-id="66cff-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66cff-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66cff-120">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="66cff-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="66cff-121">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ nomoredata.</span><span class="sxs-lookup"><span data-stu-id="66cff-121">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="66cff-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66cff-122">Requirements</span></span>



| <span data-ttu-id="66cff-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66cff-123">Requirement</span></span> | <span data-ttu-id="66cff-124">Wert</span><span class="sxs-lookup"><span data-stu-id="66cff-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66cff-125">Header</span><span class="sxs-lookup"><span data-stu-id="66cff-125">Header</span></span><br/>  | <dl> <span data-ttu-id="66cff-126"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="66cff-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="66cff-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="66cff-127">Library</span></span><br/> | <dl> <span data-ttu-id="66cff-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66cff-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66cff-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66cff-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66cff-130">Idirectxfilebinary</span><span class="sxs-lookup"><span data-stu-id="66cff-130">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
