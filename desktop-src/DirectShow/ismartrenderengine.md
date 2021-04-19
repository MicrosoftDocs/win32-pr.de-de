---
description: Die ismartrenderengine-Schnittstelle stellt Methoden bereit, die eine intelligente Neukomprimierung in DirectShow-Bearbeitungs Diensten unterstützen. Diese Schnittstelle wird von der intelligenten Rendering-Engine
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Ismartrenderengine-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370058"
---
# <a name="ismartrenderengine-interface"></a><span data-ttu-id="180c2-104">Ismartrenderengine-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="180c2-104">ISmartRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="180c2-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="180c2-105">\[Deprecated.</span></span> <span data-ttu-id="180c2-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="180c2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="180c2-107">Die- `ISmartRenderEngine` Schnittstelle stellt Methoden bereit, die eine intelligente Neukomprimierung in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="180c2-107">The `ISmartRenderEngine` interface provides methods that support smart recompression in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="180c2-108">Diese Schnittstelle wird von der intelligenten Rendering-Engine</span><span class="sxs-lookup"><span data-stu-id="180c2-108">The smart render engine exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="180c2-109">Member</span><span class="sxs-lookup"><span data-stu-id="180c2-109">Members</span></span>

<span data-ttu-id="180c2-110">Die **ismartrenderengine** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="180c2-110">The **ISmartRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="180c2-111">**Ismartrenderengine** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="180c2-111">**ISmartRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="180c2-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="180c2-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="180c2-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="180c2-113">Methods</span></span>

<span data-ttu-id="180c2-114">Die **ismartrenderengine** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="180c2-114">The **ISmartRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="180c2-115">Methode</span><span class="sxs-lookup"><span data-stu-id="180c2-115">Method</span></span>                                                                | <span data-ttu-id="180c2-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="180c2-116">Description</span></span>                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="180c2-117">**Getgroupcompressor**</span><span class="sxs-lookup"><span data-stu-id="180c2-117">**GetGroupCompressor**</span></span>](ismartrenderengine-getgroupcompressor.md)   | <span data-ttu-id="180c2-118">Ruft den Komprimierungs Filter für die angegebene Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="180c2-118">Retrieves the compression filter for the specified group.</span></span><br/>                 |
| [<span data-ttu-id="180c2-119">**Setfindcompressorcb**</span><span class="sxs-lookup"><span data-stu-id="180c2-119">**SetFindCompressorCB**</span></span>](ismartrenderengine-setfindcompressorcb.md) | <span data-ttu-id="180c2-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="180c2-120">Not implemented.</span></span><br/>                                                          |
| [<span data-ttu-id="180c2-121">**Setgroupcompressor**</span><span class="sxs-lookup"><span data-stu-id="180c2-121">**SetGroupCompressor**</span></span>](ismartrenderengine-setgroupcompressor.md)   | <span data-ttu-id="180c2-122">Gibt einen Komprimierungs Filter an, der beim Rendern der angegebenen Gruppe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="180c2-122">Specifies a compression filter to use when rendering the specified group.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="180c2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="180c2-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="180c2-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="180c2-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="180c2-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="180c2-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="180c2-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="180c2-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="180c2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="180c2-127">Requirements</span></span>



| <span data-ttu-id="180c2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="180c2-128">Requirement</span></span> | <span data-ttu-id="180c2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="180c2-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="180c2-130">Header</span><span class="sxs-lookup"><span data-stu-id="180c2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="180c2-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="180c2-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="180c2-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="180c2-132">Library</span></span><br/> | <dl> <span data-ttu-id="180c2-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="180c2-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="180c2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="180c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180c2-135">Rendern eines Projekts</span><span class="sxs-lookup"><span data-stu-id="180c2-135">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
