---
description: Die iamerrorlog-Schnittstelle stellt eine Rückruf Methode für die Fehler Protokollierung in DirectShow-Bearbeitungs Diensten bereit. Von des wird diese Schnittstelle nicht implementiert.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Iamerrorlog-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372328"
---
# <a name="iamerrorlog-interface"></a><span data-ttu-id="56d5f-103">Iamerrorlog-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="56d5f-103">IAMErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="56d5f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="56d5f-104">\[Deprecated.</span></span> <span data-ttu-id="56d5f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="56d5f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="56d5f-106">Die- `IAMErrorLog` Schnittstelle stellt eine Rückruf Methode für die Fehler Protokollierung in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="56d5f-106">The `IAMErrorLog` interface provides a callback method for error logging in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="56d5f-107">Von des wird diese Schnittstelle nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="56d5f-107">DES does not implement this interface.</span></span> <span data-ttu-id="56d5f-108">Um die Fehler Protokollierung auszuführen, implementieren Sie diese Schnittstelle in der Anwendung, und nennen Sie [**iamseterrorlog::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) auf der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="56d5f-108">To perform error logging, implement this interface in your application and call [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) on the timeline.</span></span> <span data-ttu-id="56d5f-109">Wenn beim Rendering des Projekts ein Fehler auftritt, ruft der die [**iamerrorlog:: LogError**](iamerrorlog-logerror.md) -Methode auf, die von der Anwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="56d5f-109">If an error occurs when you render the project, DES will call the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method implemented by your application.</span></span>

<span data-ttu-id="56d5f-110">DES protokolliert Fehler nur, wenn Sie ein Projekt mit der " [**unenderengine**](irenderengine.md) "-Schnittstelle Rendering.</span><span class="sxs-lookup"><span data-stu-id="56d5f-110">DES logs errors only when you render a project using the [**IRenderEngine**](irenderengine.md) interface.</span></span> <span data-ttu-id="56d5f-111">Wenn Sie z. b. ein Projekt als DirectShow-Filter Diagramm (GRF-Format) speichern und die Diagramm Datei wiedergeben, gibt es keine Fehler Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="56d5f-111">For example, if you save a project as a DirectShow filter graph (.grf format) and play the graph file, there is no error logging.</span></span> <span data-ttu-id="56d5f-112">Weitere Informationen zur Verwendung dieser Schnittstelle finden Sie unter [Protokollieren von Fehlern](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="56d5f-112">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="56d5f-113">Member</span><span class="sxs-lookup"><span data-stu-id="56d5f-113">Members</span></span>

<span data-ttu-id="56d5f-114">Die **iamerrorlog** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="56d5f-114">The **IAMErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="56d5f-115">**Iamerrorlog** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="56d5f-115">**IAMErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="56d5f-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="56d5f-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56d5f-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="56d5f-117">Methods</span></span>

<span data-ttu-id="56d5f-118">Die **iamerrorlog** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="56d5f-118">The **IAMErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="56d5f-119">Methode</span><span class="sxs-lookup"><span data-stu-id="56d5f-119">Method</span></span>                                   | <span data-ttu-id="56d5f-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56d5f-120">Description</span></span>               |
|:-----------------------------------------|:--------------------------|
| [<span data-ttu-id="56d5f-121">**LogError**</span><span class="sxs-lookup"><span data-stu-id="56d5f-121">**LogError**</span></span>](iamerrorlog-logerror.md) | <span data-ttu-id="56d5f-122">Protokolliert einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="56d5f-122">Logs an error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56d5f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56d5f-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56d5f-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="56d5f-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="56d5f-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="56d5f-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="56d5f-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56d5f-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56d5f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56d5f-127">Requirements</span></span>



| <span data-ttu-id="56d5f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56d5f-128">Requirement</span></span> | <span data-ttu-id="56d5f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="56d5f-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56d5f-130">Header</span><span class="sxs-lookup"><span data-stu-id="56d5f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="56d5f-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="56d5f-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="56d5f-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56d5f-132">Library</span></span><br/> | <dl> <span data-ttu-id="56d5f-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="56d5f-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
