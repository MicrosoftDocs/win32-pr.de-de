---
description: Ruft die Vorlagen-ID dieses Datei Daten Knotens ab.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'ID3DXFileSaveData:: GetType-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353401"
---
# <a name="id3dxfilesavedatagettype-method"></a><span data-ttu-id="fba5b-103">ID3DXFileSaveData:: GetType-Methode</span><span class="sxs-lookup"><span data-stu-id="fba5b-103">ID3DXFileSaveData::GetType method</span></span>

<span data-ttu-id="fba5b-104">Ruft die Vorlagen-ID dieses Datei Daten Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="fba5b-104">Retrieves the template ID of this file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba5b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fba5b-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a><span data-ttu-id="fba5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fba5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba5b-107">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fba5b-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba5b-108">Typ: **[ **GUID**](guid.md)\***</span><span class="sxs-lookup"><span data-stu-id="fba5b-108">Type: **[**GUID**](guid.md)\***</span></span>

<span data-ttu-id="fba5b-109">Ein Zeiger auf die GUID, die die Vorlage in diesem Datei Datenknoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="fba5b-109">Pointer to the GUID representing the template in this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba5b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fba5b-110">Return value</span></span>

<span data-ttu-id="fba5b-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fba5b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fba5b-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fba5b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fba5b-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badobject, D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="fba5b-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba5b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fba5b-114">Requirements</span></span>



| <span data-ttu-id="fba5b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fba5b-115">Requirement</span></span> | <span data-ttu-id="fba5b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fba5b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fba5b-117">Header</span><span class="sxs-lookup"><span data-stu-id="fba5b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fba5b-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="fba5b-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="fba5b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fba5b-119">Library</span></span><br/> | <dl> <span data-ttu-id="fba5b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fba5b-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fba5b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fba5b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba5b-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="fba5b-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




