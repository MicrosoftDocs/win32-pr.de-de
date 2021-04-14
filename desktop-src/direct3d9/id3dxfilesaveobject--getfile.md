---
description: Ruft die ID3DXFile-Schnittstelle des-Objekts ab, das dieses ID3DXFileSaveObject-Objekt erstellt hat.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'ID3DXFileSaveObject:: GetFile-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394174"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a><span data-ttu-id="29ea6-103">ID3DXFileSaveObject:: GetFile-Methode</span><span class="sxs-lookup"><span data-stu-id="29ea6-103">ID3DXFileSaveObject::GetFile method</span></span>

<span data-ttu-id="29ea6-104">Ruft die [**ID3DXFile**](id3dxfile.md) -Schnittstelle des-Objekts ab, das dieses [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="29ea6-104">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ea6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29ea6-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="29ea6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29ea6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ea6-107">*ppfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ea6-107">*ppFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ea6-108">Typ: **[ **ID3DXFile**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="29ea6-108">Type: **[**ID3DXFile**](id3dxfile.md)**</span></span>

<span data-ttu-id="29ea6-109">Adresse eines Zeigers auf ein [**ID3DXFile**](id3dxfile.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="29ea6-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ea6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29ea6-110">Return value</span></span>

<span data-ttu-id="29ea6-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="29ea6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="29ea6-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29ea6-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="29ea6-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, e \_ nointerface, e- \_ Zeiger.</span><span class="sxs-lookup"><span data-stu-id="29ea6-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, E\_NOINTERFACE, E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="29ea6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29ea6-114">Requirements</span></span>



| <span data-ttu-id="29ea6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29ea6-115">Requirement</span></span> | <span data-ttu-id="29ea6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="29ea6-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29ea6-117">Header</span><span class="sxs-lookup"><span data-stu-id="29ea6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="29ea6-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ea6-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="29ea6-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29ea6-119">Library</span></span><br/> | <dl> <span data-ttu-id="29ea6-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29ea6-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="29ea6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29ea6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ea6-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="29ea6-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




