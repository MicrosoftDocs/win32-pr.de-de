---
description: Ruft die Anzahl der untergeordneten Elemente in diesem Datei Datenobjekt ab.
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: 'ID3DXFileData:: GetChildren-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dd6932801f3d4b079efa6f1ed2688505dbd7828b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365323"
---
# <a name="id3dxfiledatagetchildren-method"></a><span data-ttu-id="8315e-103">ID3DXFileData:: GetChildren-Methode</span><span class="sxs-lookup"><span data-stu-id="8315e-103">ID3DXFileData::GetChildren method</span></span>

<span data-ttu-id="8315e-104">Ruft die Anzahl der untergeordneten Elemente in diesem Datei Datenobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="8315e-104">Retrieves the number of children in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8315e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8315e-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="8315e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8315e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8315e-107">*puichildren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8315e-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8315e-108">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8315e-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8315e-109">Adresse eines Zeigers, der die Anzahl der untergeordneten Elemente in diesem Datei Datenobjekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="8315e-109">Address of a pointer to receive the number of children in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8315e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8315e-110">Return value</span></span>

<span data-ttu-id="8315e-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8315e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8315e-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8315e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8315e-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="8315e-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="8315e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8315e-114">Requirements</span></span>



| <span data-ttu-id="8315e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8315e-115">Requirement</span></span> | <span data-ttu-id="8315e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8315e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8315e-117">Header</span><span class="sxs-lookup"><span data-stu-id="8315e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8315e-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="8315e-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="8315e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8315e-119">Library</span></span><br/> | <dl> <span data-ttu-id="8315e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8315e-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8315e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8315e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8315e-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="8315e-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
