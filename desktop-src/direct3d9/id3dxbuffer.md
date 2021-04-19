---
description: Die ID3DXBuffer-Schnittstelle wird als Datenpuffer verwendet und speichert Vertex-, Informations-und Material Informationen während der Mesh-Optimierung und-Ladevorgänge.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: ID3DXBuffer-Schnittstelle (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355810"
---
# <a name="id3dxbuffer-interface"></a><span data-ttu-id="f21e8-103">ID3DXBuffer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f21e8-103">ID3DXBuffer interface</span></span>

<span data-ttu-id="f21e8-104">Die ID3DXBuffer-Schnittstelle wird als Datenpuffer verwendet und speichert Vertex-, Informations-und Material Informationen während der Mesh-Optimierung und-Ladevorgänge.</span><span class="sxs-lookup"><span data-stu-id="f21e8-104">The ID3DXBuffer interface is used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.</span></span> <span data-ttu-id="f21e8-105">Das Buffer-Objekt wird verwendet, um beliebige Längen Daten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f21e8-105">The buffer object is used to return arbitrary length data.</span></span> <span data-ttu-id="f21e8-106">Außerdem werden Puffer Objekte zum Zurückgeben von Objektcode und Fehlermeldungen in Methoden verwendet, die Scheitelpunkt-und Pixel-Shader zusammenstellen.</span><span class="sxs-lookup"><span data-stu-id="f21e8-106">Also, buffer objects are used to return object code and error messages in methods that assemble vertex and pixel shaders.</span></span>

## <a name="members"></a><span data-ttu-id="f21e8-107">Member</span><span class="sxs-lookup"><span data-stu-id="f21e8-107">Members</span></span>

<span data-ttu-id="f21e8-108">Die **ID3DXBuffer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f21e8-108">The **ID3DXBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f21e8-109">**ID3DXBuffer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f21e8-109">**ID3DXBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="f21e8-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f21e8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f21e8-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f21e8-111">Methods</span></span>

<span data-ttu-id="f21e8-112">Die **ID3DXBuffer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f21e8-112">The **ID3DXBuffer** interface has these methods.</span></span>



| <span data-ttu-id="f21e8-113">Methode</span><span class="sxs-lookup"><span data-stu-id="f21e8-113">Method</span></span>                                                    | <span data-ttu-id="f21e8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f21e8-114">Description</span></span>                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="f21e8-115">**Getbufferpointer**</span><span class="sxs-lookup"><span data-stu-id="f21e8-115">**GetBufferPointer**</span></span>](id3dxbuffer--getbufferpointer.md) | <span data-ttu-id="f21e8-116">Ruft einen Zeiger auf die Daten im Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="f21e8-116">Retrieves a pointer to the data in the buffer.</span></span><br/>      |
| [<span data-ttu-id="f21e8-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="f21e8-117">**GetBufferSize**</span></span>](id3dxbuffer--getbuffersize.md)       | <span data-ttu-id="f21e8-118">Ruft die Gesamtgröße der Daten im Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="f21e8-118">Retrieves the total size of the data in the buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f21e8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f21e8-119">Remarks</span></span>

<span data-ttu-id="f21e8-120">Die **ID3DXBuffer** -Schnittstelle wird durch Aufrufen der [**D3DXCreateBuffer**](d3dxcreatebuffer.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f21e8-120">The **ID3DXBuffer** interface is obtained by calling the [**D3DXCreateBuffer**](d3dxcreatebuffer.md) function.</span></span>

<span data-ttu-id="f21e8-121">Der LPD3DXBUFFER-Typ wird als Zeiger auf die **ID3DXBuffer** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="f21e8-121">The LPD3DXBUFFER type is defined as a pointer to the **ID3DXBuffer** interface.</span></span>


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="f21e8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f21e8-122">Requirements</span></span>



| <span data-ttu-id="f21e8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f21e8-123">Requirement</span></span> | <span data-ttu-id="f21e8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f21e8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f21e8-125">Header</span><span class="sxs-lookup"><span data-stu-id="f21e8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f21e8-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f21e8-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f21e8-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f21e8-127">Library</span></span><br/> | <dl> <span data-ttu-id="f21e8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f21e8-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f21e8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f21e8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21e8-130">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f21e8-130">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
