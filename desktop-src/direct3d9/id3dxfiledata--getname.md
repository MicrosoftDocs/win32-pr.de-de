---
description: Ruft den Namen dieses Datei Datenobjekts ab.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'ID3DXFileData:: GetName-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366665"
---
# <a name="id3dxfiledatagetname-method"></a><span data-ttu-id="a91bb-103">ID3DXFileData:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="a91bb-103">ID3DXFileData::GetName method</span></span>

<span data-ttu-id="a91bb-104">Ruft den Namen dieses Datei Datenobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="a91bb-104">Retrieves the name of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a91bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a91bb-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="a91bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a91bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a91bb-107">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a91bb-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91bb-108">Typ: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a91bb-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a91bb-109">Adresse eines Zeigers, der den Namen dieses Datei Datenobjekts empfängt.</span><span class="sxs-lookup"><span data-stu-id="a91bb-109">Address of a pointer to receive the name of this file data object.</span></span> <span data-ttu-id="a91bb-110">Wenn dieser Parameter **null** ist, gibt puisize die Größe der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="a91bb-110">If this parameter is **NULL**, then puiSize will return the size of the string.</span></span> <span data-ttu-id="a91bb-111">Wenn szName auf gültigen Speicher verweist, wird der Name dieses Datei Datenobjekts bis zu der Anzahl der Zeichen, die von puisize angegeben werden, in szName kopiert.</span><span class="sxs-lookup"><span data-stu-id="a91bb-111">If szName points to valid memory, the name of this file data object will be copied into szName up to the number of characters given by puiSize.</span></span>

</dd> <dt>

<span data-ttu-id="a91bb-112">*puisize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a91bb-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a91bb-113">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a91bb-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a91bb-114">Ein Zeiger auf die Größe der Zeichenfolge, die den Namen dieses Datei Datenobjekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="a91bb-114">Pointer to the size of the string that represents the name of this file data object.</span></span> <span data-ttu-id="a91bb-115">Dieser Parameter kann **null** sein, wenn szName einen Verweis auf den Namen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a91bb-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="a91bb-116">Dieser Parameter gibt die Größe der Zeichenfolge zurück, wenn szName **null** ist.</span><span class="sxs-lookup"><span data-stu-id="a91bb-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a91bb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a91bb-117">Return value</span></span>

<span data-ttu-id="a91bb-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a91bb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a91bb-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a91bb-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a91bb-120">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="a91bb-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="a91bb-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a91bb-121">Remarks</span></span>

<span data-ttu-id="a91bb-122">Damit diese Methode erfolgreich ausgeführt werden kann, muss "szName" oder " *puisize* " nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a91bb-122">For this method to succeed, either szName or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a91bb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a91bb-123">Requirements</span></span>



| <span data-ttu-id="a91bb-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a91bb-124">Requirement</span></span> | <span data-ttu-id="a91bb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a91bb-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a91bb-126">Header</span><span class="sxs-lookup"><span data-stu-id="a91bb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a91bb-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="a91bb-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a91bb-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a91bb-128">Library</span></span><br/> | <dl> <span data-ttu-id="a91bb-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a91bb-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a91bb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a91bb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91bb-131">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="a91bb-131">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
