---
description: Ruft die Vorlagen-ID in diesem Datei Datenobjekt ab.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'ID3DXFileData:: GetType-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394189"
---
# <a name="id3dxfiledatagettype-method"></a><span data-ttu-id="79a43-103">ID3DXFileData:: GetType-Methode</span><span class="sxs-lookup"><span data-stu-id="79a43-103">ID3DXFileData::GetType method</span></span>

<span data-ttu-id="79a43-104">Ruft die Vorlagen-ID in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="79a43-104">Retrieves the template ID in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="79a43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79a43-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a><span data-ttu-id="79a43-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79a43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79a43-107">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79a43-107">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79a43-108">Typ: Konstante **[**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="79a43-108">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="79a43-109">Ein Zeiger auf die GUID, die die Vorlage in diesem Datei Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="79a43-109">Pointer to the GUID representing the template in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79a43-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79a43-110">Return value</span></span>

<span data-ttu-id="79a43-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79a43-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79a43-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79a43-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="79a43-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="79a43-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="79a43-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79a43-114">Requirements</span></span>



| <span data-ttu-id="79a43-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79a43-115">Requirement</span></span> | <span data-ttu-id="79a43-116">Wert</span><span class="sxs-lookup"><span data-stu-id="79a43-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79a43-117">Header</span><span class="sxs-lookup"><span data-stu-id="79a43-117">Header</span></span><br/>  | <dl> <span data-ttu-id="79a43-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="79a43-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="79a43-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79a43-119">Library</span></span><br/> | <dl> <span data-ttu-id="79a43-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79a43-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="79a43-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79a43-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79a43-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="79a43-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




