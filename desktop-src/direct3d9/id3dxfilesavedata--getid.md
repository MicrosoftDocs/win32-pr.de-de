---
description: Ruft die GUID dieses ID3DXFileSaveData File Data-Knotens ab.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'ID3DXFileSaveData:: GetId-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353378"
---
# <a name="id3dxfilesavedatagetid-method"></a><span data-ttu-id="96aa7-103">ID3DXFileSaveData:: GetId-Methode</span><span class="sxs-lookup"><span data-stu-id="96aa7-103">ID3DXFileSaveData::GetId method</span></span>

<span data-ttu-id="96aa7-104">Ruft die GUID dieses [**ID3DXFileSaveData**](id3dxfilesavedata.md) File Data-Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="96aa7-104">Retrieves the GUID of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="96aa7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96aa7-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="96aa7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96aa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96aa7-107">*pId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="96aa7-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96aa7-108">Typ: **lpguid**</span><span class="sxs-lookup"><span data-stu-id="96aa7-108">Type: **LPGUID**</span></span>

<span data-ttu-id="96aa7-109">Zeiger auf eine GUID, die die ID dieses Datei Daten Knotens empfängt.</span><span class="sxs-lookup"><span data-stu-id="96aa7-109">Pointer to a GUID to receive the ID of this file data node.</span></span> <span data-ttu-id="96aa7-110">Wenn das Objekt keine ID hat, ist der zurückgegebene Parameterwert GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="96aa7-110">If the object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96aa7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96aa7-111">Return value</span></span>

<span data-ttu-id="96aa7-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96aa7-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96aa7-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96aa7-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="96aa7-114">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="96aa7-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="96aa7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96aa7-115">Requirements</span></span>



| <span data-ttu-id="96aa7-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96aa7-116">Requirement</span></span> | <span data-ttu-id="96aa7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="96aa7-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96aa7-118">Header</span><span class="sxs-lookup"><span data-stu-id="96aa7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="96aa7-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="96aa7-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="96aa7-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96aa7-120">Library</span></span><br/> | <dl> <span data-ttu-id="96aa7-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96aa7-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="96aa7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96aa7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96aa7-123">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="96aa7-123">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




