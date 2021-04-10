---
description: Ruft einen Zeiger auf diesen ID3DXFileSaveObject File Data-Knoten ab.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'ID3DXFileSaveData:: getsave-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219691"
---
# <a name="id3dxfilesavedatagetsave-method"></a><span data-ttu-id="d2608-103">ID3DXFileSaveData:: getsave-Methode</span><span class="sxs-lookup"><span data-stu-id="d2608-103">ID3DXFileSaveData::GetSave method</span></span>

<span data-ttu-id="d2608-104">Ruft einen Zeiger auf diesen [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) File Data-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="d2608-104">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2608-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2608-105">Syntax</span></span>


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="d2608-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2608-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2608-107">*ppobj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d2608-107">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2608-108">Typ: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d2608-108">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="d2608-109">Adresse eines Zeigers auf eine [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Schnittstelle, die diesen Datei Datenknoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2608-109">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface representing this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2608-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2608-110">Return value</span></span>

<span data-ttu-id="d2608-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2608-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2608-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2608-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d2608-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="d2608-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2608-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2608-114">Requirements</span></span>



| <span data-ttu-id="d2608-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2608-115">Requirement</span></span> | <span data-ttu-id="d2608-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d2608-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2608-117">Header</span><span class="sxs-lookup"><span data-stu-id="d2608-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d2608-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2608-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d2608-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d2608-119">Library</span></span><br/> | <dl> <span data-ttu-id="d2608-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2608-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d2608-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2608-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2608-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="d2608-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




