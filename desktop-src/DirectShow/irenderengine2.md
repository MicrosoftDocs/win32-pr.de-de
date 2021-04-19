---
description: Die IRenderEngine2-Schnittstelle ermöglicht es der Anwendung, den von DirectShow-Bearbeitungs Diensten (des) verwendeten Standardfilter für die Videogröße zu ersetzen. Diese Schnittstelle wird von der grundlegenden Renderingengine und der intelligenten Rendering-Engine unterstützt
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: IRenderEngine2-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358753"
---
# <a name="irenderengine2-interface"></a><span data-ttu-id="7ae29-104">IRenderEngine2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7ae29-104">IRenderEngine2 interface</span></span>

> [!Note]  
> <span data-ttu-id="7ae29-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7ae29-105">\[Deprecated.</span></span> <span data-ttu-id="7ae29-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7ae29-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ae29-107">Die- `IRenderEngine2` Schnittstelle ermöglicht es der Anwendung, den von DirectShow-Bearbeitungs Diensten (des) verwendeten Standardfilter für die Videogröße zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7ae29-107">The `IRenderEngine2` interface enables the application to replace the default video resizing filter used by DirectShow Editing Services (DES).</span></span> <span data-ttu-id="7ae29-108">Diese Schnittstelle wird von der [grundlegenden Renderingengine](basic-render-engine.md) und der [intelligenten Rendering-Engine](smart-render-engine.md) unterstützt</span><span class="sxs-lookup"><span data-stu-id="7ae29-108">The [Basic Render Engine](basic-render-engine.md) and the [Smart Render Engine](smart-render-engine.md) both support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="7ae29-109">Member</span><span class="sxs-lookup"><span data-stu-id="7ae29-109">Members</span></span>

<span data-ttu-id="7ae29-110">Die **IRenderEngine2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7ae29-110">The **IRenderEngine2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7ae29-111">**IRenderEngine2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7ae29-111">**IRenderEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="7ae29-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7ae29-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7ae29-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="7ae29-113">Methods</span></span>

<span data-ttu-id="7ae29-114">Die **IRenderEngine2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7ae29-114">The **IRenderEngine2** interface has these methods.</span></span>



| <span data-ttu-id="7ae29-115">Methode</span><span class="sxs-lookup"><span data-stu-id="7ae29-115">Method</span></span>                                                  | <span data-ttu-id="7ae29-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ae29-116">Description</span></span>                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae29-117">**Abbild-GUID**</span><span class="sxs-lookup"><span data-stu-id="7ae29-117">**SetResizerGUID**</span></span>](irenderengine2-setresizerguid.md) | <span data-ttu-id="7ae29-118">Gibt die CLSID eines benutzerdefinierten Größenänderung Filters an, der von der Anwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7ae29-118">Specifies the CLSID of a custom resizing filter provided by the application.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ae29-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ae29-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ae29-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7ae29-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ae29-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7ae29-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ae29-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ae29-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ae29-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ae29-123">Requirements</span></span>



| <span data-ttu-id="7ae29-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ae29-124">Requirement</span></span> | <span data-ttu-id="7ae29-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7ae29-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae29-126">Version</span><span class="sxs-lookup"><span data-stu-id="7ae29-126">Version</span></span><br/> | <span data-ttu-id="7ae29-127">DirectX 9,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7ae29-127">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="7ae29-128">Header</span><span class="sxs-lookup"><span data-stu-id="7ae29-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7ae29-129"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7ae29-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ae29-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ae29-130">Library</span></span><br/> | <dl> <span data-ttu-id="7ae29-131"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7ae29-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae29-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ae29-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae29-133">Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe</span><span class="sxs-lookup"><span data-stu-id="7ae29-133">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
