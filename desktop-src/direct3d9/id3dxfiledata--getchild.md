---
description: Ruft ein untergeordnetes-Objekt in diesem Datei Datenobjekt ab.
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: 'ID3DXFileData:: GetChild-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 37982ca1e4801b7d70bec503ff9510fc66772651
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961662"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="a5149-103">ID3DXFileData:: GetChild-Methode</span><span class="sxs-lookup"><span data-stu-id="a5149-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="a5149-104">Ruft ein untergeordnetes-Objekt in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="a5149-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5149-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5149-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="a5149-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5149-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5149-107">*uichild* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5149-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5149-108">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5149-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5149-109">ID des abzurufenden untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="a5149-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a5149-110">*ppchild* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5149-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5149-111">Typ: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a5149-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="a5149-112">Adresse eines Zeigers, der den Schnittstellen Zeiger des untergeordneten Objekts empfängt.</span><span class="sxs-lookup"><span data-stu-id="a5149-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5149-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5149-113">Return value</span></span>

<span data-ttu-id="a5149-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5149-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5149-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5149-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a5149-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DXFERR \_ badvalue, D3DXFERR \_ nomoreobjects.</span><span class="sxs-lookup"><span data-stu-id="a5149-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5149-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5149-117">Requirements</span></span>



| <span data-ttu-id="a5149-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5149-118">Requirement</span></span> | <span data-ttu-id="a5149-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a5149-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5149-120">Header</span><span class="sxs-lookup"><span data-stu-id="a5149-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a5149-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5149-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a5149-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5149-122">Library</span></span><br/> | <dl> <span data-ttu-id="a5149-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5149-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a5149-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5149-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5149-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="a5149-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
