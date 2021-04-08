---
description: Ruft die GUID dieses Datei Datenobjekts ab.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'ID3DXFileData:: GetId-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762147"
---
# <a name="id3dxfiledatagetid-method"></a><span data-ttu-id="578ae-103">ID3DXFileData:: GetId-Methode</span><span class="sxs-lookup"><span data-stu-id="578ae-103">ID3DXFileData::GetId method</span></span>

<span data-ttu-id="578ae-104">Ruft die GUID dieses Datei Datenobjekts ab.</span><span class="sxs-lookup"><span data-stu-id="578ae-104">Retrieves the GUID of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="578ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="578ae-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="578ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="578ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="578ae-107">*pId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="578ae-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="578ae-108">Typ: **lpguid**</span><span class="sxs-lookup"><span data-stu-id="578ae-108">Type: **LPGUID**</span></span>

<span data-ttu-id="578ae-109">Zeiger auf eine GUID, die die ID dieses Datei Datenobjekts empfängt.</span><span class="sxs-lookup"><span data-stu-id="578ae-109">Pointer to a GUID to receive the ID of this file data object.</span></span> <span data-ttu-id="578ae-110">Wenn das Datei Datenobjekt keine ID hat, ist der zurückgegebene Parameterwert GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="578ae-110">If the file data object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="578ae-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="578ae-111">Return value</span></span>

<span data-ttu-id="578ae-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="578ae-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="578ae-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="578ae-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="578ae-114">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="578ae-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="578ae-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="578ae-115">Requirements</span></span>



| <span data-ttu-id="578ae-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="578ae-116">Requirement</span></span> | <span data-ttu-id="578ae-117">Wert</span><span class="sxs-lookup"><span data-stu-id="578ae-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="578ae-118">Header</span><span class="sxs-lookup"><span data-stu-id="578ae-118">Header</span></span><br/>  | <dl> <span data-ttu-id="578ae-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="578ae-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="578ae-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="578ae-120">Library</span></span><br/> | <dl> <span data-ttu-id="578ae-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="578ae-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="578ae-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="578ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578ae-123">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="578ae-123">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




