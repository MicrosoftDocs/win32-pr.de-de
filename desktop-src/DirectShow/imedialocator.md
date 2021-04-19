---
description: Die imedialocator-Schnittstelle stellt Methoden zum Validieren von Dateinamen in DirectShow-Bearbeitungs Diensten bereit.
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Imedialocator-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366891"
---
# <a name="imedialocator-interface"></a><span data-ttu-id="76c9c-103">Imedialocator-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="76c9c-103">IMediaLocator interface</span></span>

> [!Note]  
> <span data-ttu-id="76c9c-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="76c9c-104">\[Deprecated.</span></span> <span data-ttu-id="76c9c-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="76c9c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="76c9c-106">Die- `IMediaLocator` Schnittstelle stellt Methoden zum Validieren von Dateinamen in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="76c9c-106">The `IMediaLocator` interface provides methods for validating file names in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="76c9c-107">Verwenden Sie diese Schnittstelle, um sicherzustellen, dass der angegebene Dateiname und der Pfad einer vorhandenen Datei entsprechen.</span><span class="sxs-lookup"><span data-stu-id="76c9c-107">Use this interface to ensure that a given file name and path correspond to an existing file.</span></span> <span data-ttu-id="76c9c-108">Diese Schnittstelle bietet auch eine Möglichkeit, um an anderen Speicherorten nach der Datei zu suchen und ein Dialogfeld **Öffnen** anzuzeigen, in dem der Benutzer die Datei finden kann.</span><span class="sxs-lookup"><span data-stu-id="76c9c-108">This interface also provides a way to search for the file at other locations, and to display an **Open** dialog box so that the user can locate the file.</span></span>

<span data-ttu-id="76c9c-109">Der medienlocator implementiert diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="76c9c-109">The media locator implements this interface.</span></span> <span data-ttu-id="76c9c-110">Die Zeitachse und die Rendering-Engine unterstützen auch die Überprüfung von Dateinamen mithilfe der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="76c9c-110">The timeline and the render engine also support file name validation through the following methods:</span></span>

-   <span data-ttu-id="76c9c-111">[**Iamtimeline:: validatesourcenames**](iamtimeline-validatesourcenames.md): überprüft und aktualisiert Dateinamen in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="76c9c-111">[**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md): Validates and updates file names in the timeline.</span></span>
-   <span data-ttu-id="76c9c-112">[**Alienderengine:: setsourcenamevalidation**](irenderengine-setsourcenamevalidation.md): gibt an, wie die Renderingengine Dateinamen zur Renderingzeit überprüft.</span><span class="sxs-lookup"><span data-stu-id="76c9c-112">[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): Specifies how the render engine validates file names at rendering time.</span></span>

<span data-ttu-id="76c9c-113">In der Regel wird diese Methode von einer des-Anwendung aufgerufen, anstatt direkt eine Instanz des medienlocators zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76c9c-113">Typically, a DES application will call these methods rather than directly create an instance of the media locator.</span></span> <span data-ttu-id="76c9c-114">Weitere Informationen finden Sie unter [using the Media Locator](using-the-media-locator.md).</span><span class="sxs-lookup"><span data-stu-id="76c9c-114">For more information, see [Using the Media Locator](using-the-media-locator.md).</span></span>

## <a name="members"></a><span data-ttu-id="76c9c-115">Member</span><span class="sxs-lookup"><span data-stu-id="76c9c-115">Members</span></span>

<span data-ttu-id="76c9c-116">Die **imedialocator** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="76c9c-116">The **IMediaLocator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="76c9c-117">**Imedialocator** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="76c9c-117">**IMediaLocator** also has these types of members:</span></span>

-   [<span data-ttu-id="76c9c-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="76c9c-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="76c9c-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="76c9c-119">Methods</span></span>

<span data-ttu-id="76c9c-120">Die **imedialocator** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="76c9c-120">The **IMediaLocator** interface has these methods.</span></span>



| <span data-ttu-id="76c9c-121">Methode</span><span class="sxs-lookup"><span data-stu-id="76c9c-121">Method</span></span>                                                     | <span data-ttu-id="76c9c-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76c9c-122">Description</span></span>                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="76c9c-123">**Addfoundlocation**</span><span class="sxs-lookup"><span data-stu-id="76c9c-123">**AddFoundLocation**</span></span>](imedialocator-addfoundlocation.md) | <span data-ttu-id="76c9c-124">Fügt dem Verzeichnis Cache ein Verzeichnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="76c9c-124">Adds a directory to the directory cache.</span></span><br/>                                |
| [<span data-ttu-id="76c9c-125">**Findmediafile**</span><span class="sxs-lookup"><span data-stu-id="76c9c-125">**FindMediaFile**</span></span>](imedialocator-findmediafile.md)       | <span data-ttu-id="76c9c-126">Sucht nach einer Datei und ruft, wenn erfolgreich, den Pfad zur Datei ab.</span><span class="sxs-lookup"><span data-stu-id="76c9c-126">Searches for a file and, if successful, retrieves the path to the file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76c9c-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76c9c-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="76c9c-128">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="76c9c-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="76c9c-129">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="76c9c-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="76c9c-130">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76c9c-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="76c9c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76c9c-131">Requirements</span></span>



| <span data-ttu-id="76c9c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76c9c-132">Requirement</span></span> | <span data-ttu-id="76c9c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="76c9c-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76c9c-134">Header</span><span class="sxs-lookup"><span data-stu-id="76c9c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="76c9c-135"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="76c9c-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="76c9c-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76c9c-136">Library</span></span><br/> | <dl> <span data-ttu-id="76c9c-137"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="76c9c-137"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
