---
description: Commit für alle an einem Mesh vorgenommenen Änderungen auf dem Gerät durchgeführt, sodass die Änderungen gerendert werden können. Dies sollte aufgerufen werden, nachdem die Daten eines Netzes geändert wurden und bevor es gerendert wird. Ein Mesh kann nur dann gerendert werden, wenn es auf dem Gerät ausgeführt wird. Siehe Bemerkungen.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'ID3DX10Mesh:: commitondevice-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050864"
---
# <a name="id3dx10meshcommittodevice-method"></a><span data-ttu-id="f1da7-106">ID3DX10Mesh:: committo Device-Methode</span><span class="sxs-lookup"><span data-stu-id="f1da7-106">ID3DX10Mesh::CommitToDevice method</span></span>

<span data-ttu-id="f1da7-107">Commit für alle an einem Mesh vorgenommenen Änderungen auf dem Gerät durchgeführt, sodass die Änderungen gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="f1da7-107">Commit any changes made to a mesh to the device so that the changes can be rendered.</span></span> <span data-ttu-id="f1da7-108">Dies sollte aufgerufen werden, nachdem die Daten eines Netzes geändert wurden und bevor es gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="f1da7-108">This should be called after a mesh's data is altered and before it is rendered.</span></span> <span data-ttu-id="f1da7-109">Ein Mesh kann nur dann gerendert werden, wenn es auf dem Gerät ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1da7-109">A mesh cannot be rendered unless it is committed to the device.</span></span> <span data-ttu-id="f1da7-110">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="f1da7-110">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1da7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1da7-111">Syntax</span></span>


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a><span data-ttu-id="f1da7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1da7-112">Parameters</span></span>

<span data-ttu-id="f1da7-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f1da7-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1da7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1da7-114">Return value</span></span>

<span data-ttu-id="f1da7-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1da7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1da7-116">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f1da7-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1da7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1da7-117">Remarks</span></span>

<span data-ttu-id="f1da7-118">Wenn ein Mesh geladen wird, werden die Daten in stagingressourcen geladen, was bedeutet, dass die Daten geändert, aber nicht gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="f1da7-118">When a mesh is loaded, it's data is loaded into staging resources, meaning the data can be altered but not rendered.</span></span> <span data-ttu-id="f1da7-119">Wenn committo Device aufgerufen wird, werden die Daten aus den stagingressourcen in Geräte Ressourcen kopiert, sodass Sie gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="f1da7-119">When CommitToDevice is called, the data from the staging resources are copied into device resources so that they can be rendered.</span></span> <span data-ttu-id="f1da7-120">Obwohl die Daten auf dem Gerät committet werden, verbleiben die stagingressourcen und können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f1da7-120">Although the data is committed to the device, the staging resources remain and can be modified.</span></span> <span data-ttu-id="f1da7-121">Wenn Änderungen an den stagingressourcen vorgenommen werden, müssen die stagingressourcen erneut an das Gerät übertragen werden, damit diese Änderungen auf dem Bildschirm gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="f1da7-121">If any modifications are made to the staging resources, the staging resources must be committed to the device again in order for those changes to be rendered on screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1da7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1da7-122">Requirements</span></span>



| <span data-ttu-id="f1da7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1da7-123">Requirement</span></span> | <span data-ttu-id="f1da7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f1da7-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1da7-125">Header</span><span class="sxs-lookup"><span data-stu-id="f1da7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f1da7-126"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1da7-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1da7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f1da7-127">Library</span></span><br/> | <dl> <span data-ttu-id="f1da7-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1da7-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1da7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1da7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1da7-130">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="f1da7-130">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="f1da7-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f1da7-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




