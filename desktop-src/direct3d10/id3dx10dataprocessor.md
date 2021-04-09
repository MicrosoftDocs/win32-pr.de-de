---
description: Datenverarbeitungs Objekt, das von der ID3DX10ThreadPump-Schnittstelle zum asynchronen verarbeiten geladener Daten verwendet wird.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: ID3DX10DataProcessor-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870212"
---
# <a name="id3dx10dataprocessor-interface"></a><span data-ttu-id="fb39c-103">ID3DX10DataProcessor-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fb39c-103">ID3DX10DataProcessor interface</span></span>

<span data-ttu-id="fb39c-104">Datenverarbeitungs Objekt, das von der [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen verarbeiten geladener Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb39c-104">Data processing object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for processing loaded data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="fb39c-105">Member</span><span class="sxs-lookup"><span data-stu-id="fb39c-105">Members</span></span>

<span data-ttu-id="fb39c-106">Die **ID3DX10DataProcessor** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fb39c-106">The **ID3DX10DataProcessor** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fb39c-107">**ID3DX10DataProcessor** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb39c-107">**ID3DX10DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="fb39c-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="fb39c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fb39c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="fb39c-109">Methods</span></span>

<span data-ttu-id="fb39c-110">Die **ID3DX10DataProcessor** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fb39c-110">The **ID3DX10DataProcessor** interface has these methods.</span></span>



| <span data-ttu-id="fb39c-111">Methode</span><span class="sxs-lookup"><span data-stu-id="fb39c-111">Method</span></span>                                                                | <span data-ttu-id="fb39c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb39c-112">Description</span></span>                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb39c-113">**"Kreatedeviceobject"**</span><span class="sxs-lookup"><span data-stu-id="fb39c-113">**CreateDeviceObject**</span></span>](id3dx10dataprocessor-createdeviceobject.md) | <span data-ttu-id="fb39c-114">Erstellen Sie ein Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="fb39c-114">Create a device object.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="fb39c-115">**Zerstören**</span><span class="sxs-lookup"><span data-stu-id="fb39c-115">**Destroy**</span></span>](id3dx10dataprocessor-destroy.md)                       | <span data-ttu-id="fb39c-116">Wird von einer [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) verwendet, um den Prozessor zu zerstören, nachdem ein Arbeits Element abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fb39c-116">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the processor after a work item completes.</span></span><br/> |
| [<span data-ttu-id="fb39c-117">**Prozess**</span><span class="sxs-lookup"><span data-stu-id="fb39c-117">**Process**</span></span>](id3dx10dataprocessor-process.md)                       | <span data-ttu-id="fb39c-118">Verarbeiten einiger Daten.</span><span class="sxs-lookup"><span data-stu-id="fb39c-118">Process some data.</span></span><br/>                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="fb39c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb39c-119">Remarks</span></span>

<span data-ttu-id="fb39c-120">Dieses Objekt kann geerbt und seine Member neu definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb39c-120">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="fb39c-121">Auf diese Weise können Sie die API für die Verarbeitung Ihrer eigenen benutzerdefinierten Dateiformate anpassen.</span><span class="sxs-lookup"><span data-stu-id="fb39c-121">Doing so would enable you to customize the API for processing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb39c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb39c-122">Requirements</span></span>



| <span data-ttu-id="fb39c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb39c-123">Requirement</span></span> | <span data-ttu-id="fb39c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fb39c-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb39c-125">Header</span><span class="sxs-lookup"><span data-stu-id="fb39c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fb39c-126"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb39c-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb39c-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb39c-127">Library</span></span><br/> | <dl> <span data-ttu-id="fb39c-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb39c-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb39c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb39c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb39c-130">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="fb39c-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
