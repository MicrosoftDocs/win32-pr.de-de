---
description: Die scrapit-Methode verwirft das Filter Diagramm der Rendering-Engine und alle zugeordneten Objekte.
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: 'Unenderengine:: scrapit-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f9febbe20cfd5ab9a6577a6e00989c7d6fc4145
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362122"
---
# <a name="irenderenginescrapit-method"></a><span data-ttu-id="cad0a-103">Unenderengine:: scrapit-Methode</span><span class="sxs-lookup"><span data-stu-id="cad0a-103">IRenderEngine::ScrapIt method</span></span>

> [!Note]  
> <span data-ttu-id="cad0a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cad0a-104">\[Deprecated.</span></span> <span data-ttu-id="cad0a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cad0a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cad0a-106">Die `ScrapIt` -Methode verwirft das Filter Diagramm der Renderengine und alle zugeordneten Objekte.</span><span class="sxs-lookup"><span data-stu-id="cad0a-106">The `ScrapIt` method discards the render engine's filter graph and all associated objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad0a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad0a-107">Syntax</span></span>


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a><span data-ttu-id="cad0a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cad0a-108">Parameters</span></span>

<span data-ttu-id="cad0a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cad0a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cad0a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cad0a-110">Return value</span></span>

<span data-ttu-id="cad0a-111">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="cad0a-111">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="cad0a-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cad0a-112">Return code</span></span>                                                                                            | <span data-ttu-id="cad0a-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cad0a-113">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="cad0a-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cad0a-114"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="cad0a-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cad0a-115">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="cad0a-116"><dt>**E \_ muss \_ Init \_ Renderer**</dt></span><span class="sxs-lookup"><span data-stu-id="cad0a-116"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="cad0a-117">Fehler beim Initialisieren der Rendering-Engine.</span><span class="sxs-lookup"><span data-stu-id="cad0a-117">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cad0a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cad0a-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cad0a-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cad0a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cad0a-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cad0a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cad0a-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cad0a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cad0a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cad0a-122">Requirements</span></span>



| <span data-ttu-id="cad0a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cad0a-123">Requirement</span></span> | <span data-ttu-id="cad0a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cad0a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cad0a-125">Header</span><span class="sxs-lookup"><span data-stu-id="cad0a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cad0a-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cad0a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cad0a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cad0a-127">Library</span></span><br/> | <dl> <span data-ttu-id="cad0a-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cad0a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad0a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cad0a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad0a-130">**Schnittstelle ""**</span><span class="sxs-lookup"><span data-stu-id="cad0a-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="cad0a-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="cad0a-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




