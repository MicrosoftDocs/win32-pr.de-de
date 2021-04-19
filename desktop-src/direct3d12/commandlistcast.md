---
title: Commandlistcast-Funktion (D3dx12. h)
description: Diese Funktions Vorlage wandelt einen Konstanten Zeiger auf eine beliebige Befehlsliste in einen Konstanten Zeiger auf einen ID3D12CommandList um.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- Commandlistcast-Funktion
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350725"
---
# <a name="commandlistcast-function"></a><span data-ttu-id="0ba6d-104">Commandlistcast-Funktion</span><span class="sxs-lookup"><span data-stu-id="0ba6d-104">CommandListCast function</span></span>

<span data-ttu-id="0ba6d-105">Diese Funktions Vorlage wandelt einen Konstanten Zeiger auf eine beliebige Befehlsliste in einen Konstanten Zeiger auf einen ID3D12CommandList um.</span><span class="sxs-lookup"><span data-stu-id="0ba6d-105">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span>

<span data-ttu-id="0ba6d-106">Diese Umwandlung ist nützlich zum Übergeben von stark typisierten Befehlslisten Zeigern an [**executecommandlists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="0ba6d-106">This cast is useful for passing strongly-typed command list pointers into [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba6d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ba6d-107">Syntax</span></span>


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a><span data-ttu-id="0ba6d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ba6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba6d-109">*Trupp*</span><span class="sxs-lookup"><span data-stu-id="0ba6d-109">*pp*</span></span> 
</dt> <dd>

<span data-ttu-id="0ba6d-110">Typ: **t \_ commandlisttype \* \* konstant**</span><span class="sxs-lookup"><span data-stu-id="0ba6d-110">Type: **t\_CommandListType \* const \***</span></span>

<span data-ttu-id="0ba6d-111">Die stark typisierte Befehlsliste, die umgewandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ba6d-111">The strongly-typed command list to cast.</span></span>

<span data-ttu-id="0ba6d-112">Das Vorlagen Argument **t \_ commandlisttype** gibt ein beliebiges stark typisiertes Befehlslisten Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0ba6d-112">The template argument **t\_CommandListType** specifies any strongly-typed command list object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba6d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ba6d-113">Return value</span></span>

<span data-ttu-id="0ba6d-114">Typ: **ID3D12CommandList \* konstant \***</span><span class="sxs-lookup"><span data-stu-id="0ba6d-114">Type: **ID3D12CommandList \* const \***</span></span>

<span data-ttu-id="0ba6d-115">Die stark typisierte Befehlsliste, die als [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)neu interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ba6d-115">The strongly-typed command list, reinterpreted as an [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ba6d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ba6d-116">Remarks</span></span>

<span data-ttu-id="0ba6d-117">Commandlistcast führt eine **uminterpretierungsumwandlung \_** aus.</span><span class="sxs-lookup"><span data-stu-id="0ba6d-117">CommandListCast performs a **reinterpret\_cast**.</span></span> <span data-ttu-id="0ba6d-118">Die Umwandlung ist gültig, solange die Konstante der Befehlsliste respektiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ba6d-118">The cast is valid as long as the const-ness of the command list is respected.</span></span>

<span data-ttu-id="0ba6d-119">Die commandlistcast-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="0ba6d-119">The CommandListCast function is defined as the following:</span></span>


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a><span data-ttu-id="0ba6d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ba6d-120">Requirements</span></span>



| <span data-ttu-id="0ba6d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ba6d-121">Requirement</span></span> | <span data-ttu-id="0ba6d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0ba6d-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba6d-123">Header</span><span class="sxs-lookup"><span data-stu-id="0ba6d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0ba6d-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba6d-124"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="0ba6d-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ba6d-125">Library</span></span><br/> | <dl> <span data-ttu-id="0ba6d-126"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ba6d-126"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="0ba6d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0ba6d-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="0ba6d-128"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba6d-128"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba6d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ba6d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba6d-130">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="0ba6d-130">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





