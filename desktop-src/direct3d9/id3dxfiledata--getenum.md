---
description: Ruft das Enumerationsobjekt in diesem Datei Datenobjekt ab.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'ID3DXFileData:: getenum-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370445"
---
# <a name="id3dxfiledatagetenum-method"></a><span data-ttu-id="d81b1-103">ID3DXFileData:: getenum-Methode</span><span class="sxs-lookup"><span data-stu-id="d81b1-103">ID3DXFileData::GetEnum method</span></span>

<span data-ttu-id="d81b1-104">Ruft das Enumerationsobjekt in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="d81b1-104">Retrieves the enumeration object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d81b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d81b1-105">Syntax</span></span>


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="d81b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d81b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d81b1-107">*ppobj* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d81b1-107">*ppObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d81b1-108">Typ: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d81b1-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="d81b1-109">Adresse eines Zeigers, der das Enumerationsobjekt in diesem Datei Datenobjekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="d81b1-109">Address of a pointer to receive the enumeration object in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d81b1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d81b1-110">Return value</span></span>

<span data-ttu-id="d81b1-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d81b1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d81b1-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d81b1-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d81b1-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="d81b1-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d81b1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d81b1-114">Requirements</span></span>



| <span data-ttu-id="d81b1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d81b1-115">Requirement</span></span> | <span data-ttu-id="d81b1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d81b1-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d81b1-117">Header</span><span class="sxs-lookup"><span data-stu-id="d81b1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d81b1-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d81b1-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d81b1-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d81b1-119">Library</span></span><br/> | <dl> <span data-ttu-id="d81b1-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d81b1-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d81b1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d81b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d81b1-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="d81b1-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




