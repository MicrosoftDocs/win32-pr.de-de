---
description: Datenlade Objekt, das von der ID3DX10ThreadPump-Schnittstelle zum asynchronen Laden von Daten verwendet wird
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: ID3DX10DataLoader-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961616"
---
# <a name="id3dx10dataloader-interface"></a><span data-ttu-id="07077-103">ID3DX10DataLoader-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="07077-103">ID3DX10DataLoader interface</span></span>

<span data-ttu-id="07077-104">Datenlade Objekt, das von der [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen Laden von Daten verwendet wird</span><span class="sxs-lookup"><span data-stu-id="07077-104">Data loading object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="07077-105">Member</span><span class="sxs-lookup"><span data-stu-id="07077-105">Members</span></span>

<span data-ttu-id="07077-106">Die **ID3DX10DataLoader** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="07077-106">The **ID3DX10DataLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="07077-107">**ID3DX10DataLoader** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="07077-107">**ID3DX10DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="07077-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="07077-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="07077-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="07077-109">Methods</span></span>

<span data-ttu-id="07077-110">Die **ID3DX10DataLoader** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="07077-110">The **ID3DX10DataLoader** interface has these methods.</span></span>



| <span data-ttu-id="07077-111">Methode</span><span class="sxs-lookup"><span data-stu-id="07077-111">Method</span></span>                                             | <span data-ttu-id="07077-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07077-112">Description</span></span>                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07077-113">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="07077-113">**Decompress**</span></span>](id3dx10dataloader-decompress.md) | <span data-ttu-id="07077-114">Wird verwendet, um codierte Daten zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="07077-114">Used to decompress encoded data.</span></span> <span data-ttu-id="07077-115">Dies wird in der Regel zum Laden von Ressourcen aus Dateisystemen wie ZIP-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="07077-115">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="07077-116">Beim Laden von einer nicht komprimierten Ressource muss für die Debug-Phase keine Arbeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="07077-116">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span><br/> |
| [<span data-ttu-id="07077-117">**Zerstören**</span><span class="sxs-lookup"><span data-stu-id="07077-117">**Destroy**</span></span>](id3dx10dataloader-destroy.md)       | <span data-ttu-id="07077-118">Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) verwendet, um das Lade Modul zu zerstören, nachdem ein Arbeits Element abgeschlossen wurde</span><span class="sxs-lookup"><span data-stu-id="07077-118">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the loader after a work item completes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="07077-119">**Laden**</span><span class="sxs-lookup"><span data-stu-id="07077-119">**Load**</span></span>](id3dx10dataloader-load.md)             | <span data-ttu-id="07077-120">Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum Laden von Daten von einem Datenträger verwendet.</span><span class="sxs-lookup"><span data-stu-id="07077-120">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to load data from a disk.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="07077-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07077-121">Remarks</span></span>

<span data-ttu-id="07077-122">Dieses Objekt kann geerbt und seine Member neu definiert werden.</span><span class="sxs-lookup"><span data-stu-id="07077-122">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="07077-123">Auf diese Weise können Sie die API zum Laden und Dekomprimieren ihrer eigenen benutzerdefinierten Dateiformate anpassen.</span><span class="sxs-lookup"><span data-stu-id="07077-123">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="07077-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07077-124">Requirements</span></span>



| <span data-ttu-id="07077-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07077-125">Requirement</span></span> | <span data-ttu-id="07077-126">Wert</span><span class="sxs-lookup"><span data-stu-id="07077-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07077-127">Header</span><span class="sxs-lookup"><span data-stu-id="07077-127">Header</span></span><br/>  | <dl> <span data-ttu-id="07077-128"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="07077-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="07077-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07077-129">Library</span></span><br/> | <dl> <span data-ttu-id="07077-130"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07077-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07077-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07077-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07077-132">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="07077-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
