---
description: Ruft den Namen dieses ID3DXFileSaveData File Data-Knotens ab.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: 'ID3DXFileSaveData:: GetName-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00fa8c60f423343d3d4c594d31141a2f192802d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050884"
---
# <a name="id3dxfilesavedatagetname-method"></a><span data-ttu-id="a4c54-103">ID3DXFileSaveData:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="a4c54-103">ID3DXFileSaveData::GetName method</span></span>

<span data-ttu-id="a4c54-104">Ruft den Namen dieses [**ID3DXFileSaveData**](id3dxfilesavedata.md) File Data-Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="a4c54-104">Retrieves the name of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c54-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4c54-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="a4c54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4c54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c54-107">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4c54-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c54-108">Typ: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4c54-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4c54-109">Adresse eines Zeigers, der den Namen dieses Datei Daten Knotens empfängt.</span><span class="sxs-lookup"><span data-stu-id="a4c54-109">Address of a pointer to receive the name of this file data node.</span></span> <span data-ttu-id="a4c54-110">Wenn dieser Parameter **null** ist, gibt *puisize* die Größe der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="a4c54-110">If this parameter is **NULL**, then *puiSize* will return the size of the string.</span></span> <span data-ttu-id="a4c54-111">Wenn szName auf gültigen Speicher verweist, wird der Name dieses Datei Daten Knotens bis zu der Anzahl der Zeichen, die von *puisize* angegeben werden, in szName kopiert.</span><span class="sxs-lookup"><span data-stu-id="a4c54-111">If szName points to valid memory, the name of this file data node will be copied into szName up to the number of characters given by *puiSize* .</span></span>

</dd> <dt>

<span data-ttu-id="a4c54-112">*puisize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a4c54-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c54-113">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4c54-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a4c54-114">Ein Zeiger auf die Größe der Zeichenfolge, die den Namen dieses Datei Daten Knotens darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4c54-114">Pointer to the size of the string that represents the name of this file data node.</span></span> <span data-ttu-id="a4c54-115">Dieser Parameter kann **null** sein, wenn szName einen Verweis auf den Namen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a4c54-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="a4c54-116">Dieser Parameter gibt die Größe der Zeichenfolge zurück, wenn szName **null** ist.</span><span class="sxs-lookup"><span data-stu-id="a4c54-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c54-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4c54-117">Return value</span></span>

<span data-ttu-id="a4c54-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a4c54-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a4c54-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a4c54-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a4c54-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="a4c54-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c54-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4c54-121">Remarks</span></span>

<span data-ttu-id="a4c54-122">Damit diese Methode erfolgreich ausgeführt werden kann, muss " *szName* " oder " *puisize* " nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a4c54-122">For this method to succeed, either *szName* or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c54-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4c54-123">Requirements</span></span>



| <span data-ttu-id="a4c54-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4c54-124">Requirement</span></span> | <span data-ttu-id="a4c54-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a4c54-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c54-126">Header</span><span class="sxs-lookup"><span data-stu-id="a4c54-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a4c54-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c54-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a4c54-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4c54-128">Library</span></span><br/> | <dl> <span data-ttu-id="a4c54-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4c54-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a4c54-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4c54-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c54-131">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="a4c54-131">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
