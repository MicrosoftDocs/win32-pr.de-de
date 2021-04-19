---
description: 'Die iresize-Schnittstelle muss von jedem benutzerdefinierten Filter zum Ändern der Größe von Videos für DirectShow-Bearbeitungs Dienste unterstützt werden. Um einen benutzerdefinierten Filter für die Größenänderung festzulegen, müssen Sie die IRenderEngine2:: setresizerguid-Methode für die Rendering-Engine aufzurufen.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Iresize-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357553"
---
# <a name="iresize-interface"></a><span data-ttu-id="d396d-104">Iresize-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d396d-104">IResize interface</span></span>

> [!Note]  
> <span data-ttu-id="d396d-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d396d-105">\[Deprecated.</span></span> <span data-ttu-id="d396d-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d396d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d396d-107">Die `IResize` Schnittstelle muss von jedem benutzerdefinierten Filter zum Ändern der Größe von Videos für DirectShow-Bearbeitungs Dienste unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d396d-107">The `IResize` interface must be supported by any custom video resizer filter for DirectShow Editing Services (DES).</span></span> <span data-ttu-id="d396d-108">Um einen benutzerdefinierten Filter für die Größenänderung festzulegen, müssen Sie die [**IRenderEngine2:: setresizerguid**](irenderengine2-setresizerguid.md) -Methode für die Rendering-Engine aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d396d-108">To set a custom resizer filter, call the [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) method on the render engine.</span></span>

## <a name="members"></a><span data-ttu-id="d396d-109">Member</span><span class="sxs-lookup"><span data-stu-id="d396d-109">Members</span></span>

<span data-ttu-id="d396d-110">Die **iresize** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d396d-110">The **IResize** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d396d-111">**Iresize** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d396d-111">**IResize** also has these types of members:</span></span>

-   [<span data-ttu-id="d396d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="d396d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d396d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d396d-113">Methods</span></span>

<span data-ttu-id="d396d-114">Die **iresize** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d396d-114">The **IResize** interface has these methods.</span></span>



| <span data-ttu-id="d396d-115">Methode</span><span class="sxs-lookup"><span data-stu-id="d396d-115">Method</span></span>                                          | <span data-ttu-id="d396d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d396d-116">Description</span></span>                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="d396d-117">**\_inputsize erhalten**</span><span class="sxs-lookup"><span data-stu-id="d396d-117">**get\_InputSize**</span></span>](iresize-get-inputsize.md) | <span data-ttu-id="d396d-118">Gibt die aktuelle Eingabe Größe des Filter der Größenänderung zurück.</span><span class="sxs-lookup"><span data-stu-id="d396d-118">Returns the resizer filter's current input size.</span></span><br/>  |
| [<span data-ttu-id="d396d-119">**\_mediaType erhalten**</span><span class="sxs-lookup"><span data-stu-id="d396d-119">**get\_MediaType**</span></span>](iresize-get-mediatype.md) | <span data-ttu-id="d396d-120">Gibt den Typ des Ausgabemediums für die Größe der Größe zurück.</span><span class="sxs-lookup"><span data-stu-id="d396d-120">Returns the resizer filter's output media type.</span></span><br/>   |
| [<span data-ttu-id="d396d-121">**\_Größe erhalten**</span><span class="sxs-lookup"><span data-stu-id="d396d-121">**get\_Size**</span></span>](iresize-get-size.md)           | <span data-ttu-id="d396d-122">Gibt die aktuelle Ausgabegröße und den streckungs Modus zurück.</span><span class="sxs-lookup"><span data-stu-id="d396d-122">Returns the current output size and stretch mode.</span></span><br/> |
| [<span data-ttu-id="d396d-123">**\_mediaType platzieren**</span><span class="sxs-lookup"><span data-stu-id="d396d-123">**put\_MediaType**</span></span>](iresize-put-mediatype.md) | <span data-ttu-id="d396d-124">Legt den Ausgabe Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="d396d-124">Sets the output media type.</span></span><br/>                       |
| [<span data-ttu-id="d396d-125">**Put \_ size**</span><span class="sxs-lookup"><span data-stu-id="d396d-125">**put\_Size**</span></span>](iresize-put-size.md)           | <span data-ttu-id="d396d-126">Legt die Ausgabegröße und den streckungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="d396d-126">Sets the output size and stretch mode.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="d396d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d396d-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d396d-128">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d396d-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d396d-129">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="d396d-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d396d-130">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d396d-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d396d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d396d-131">Requirements</span></span>



| <span data-ttu-id="d396d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d396d-132">Requirement</span></span> | <span data-ttu-id="d396d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d396d-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d396d-134">Version</span><span class="sxs-lookup"><span data-stu-id="d396d-134">Version</span></span><br/> | <span data-ttu-id="d396d-135">DirectX 9,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d396d-135">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="d396d-136">Header</span><span class="sxs-lookup"><span data-stu-id="d396d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d396d-137"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="d396d-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d396d-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d396d-138">Library</span></span><br/> | <dl> <span data-ttu-id="d396d-139"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="d396d-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d396d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d396d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d396d-141">Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe</span><span class="sxs-lookup"><span data-stu-id="d396d-141">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
