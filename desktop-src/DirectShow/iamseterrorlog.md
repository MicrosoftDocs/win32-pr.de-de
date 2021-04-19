---
description: Die iamseterrorlog-Schnittstelle legt ein Fehlerprotokoll in DirectShow-Bearbeitungs Diensten fest oder ruft es ab.
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Iamenterrorlog-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366972"
---
# <a name="iamseterrorlog-interface"></a><span data-ttu-id="56548-103">Iameinterrorlog-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="56548-103">IAMSetErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="56548-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="56548-104">\[Deprecated.</span></span> <span data-ttu-id="56548-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="56548-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="56548-106">Die- `IAMSetErrorLog` Schnittstelle legt ein Fehlerprotokoll in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="56548-106">The `IAMSetErrorLog` interface sets or retrieves an error log in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="56548-107">Das Zeitachsen Objekt implementiert diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="56548-107">The timeline object implements this interface.</span></span> <span data-ttu-id="56548-108">Anwendungen können diese Schnittstelle zum Protokollieren von renderingfehlern zur Laufzeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="56548-108">Applications can use this interface to log rendering errors at run time.</span></span> <span data-ttu-id="56548-109">Implementieren Sie die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle in der Anwendung, und nennen Sie dann die Methode [**iamseterrorlog::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) auf der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="56548-109">Implement the [**IAMErrorLog**](iamerrorlog.md) interface in your application, and then call the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span>

<span data-ttu-id="56548-110">Weitere Informationen zur Verwendung dieser Schnittstelle finden Sie unter [Protokollieren von Fehlern](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="56548-110">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="56548-111">Member</span><span class="sxs-lookup"><span data-stu-id="56548-111">Members</span></span>

<span data-ttu-id="56548-112">Die **iameinterrorlog** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="56548-112">The **IAMSetErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="56548-113">**Iamenterrorlog** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="56548-113">**IAMSetErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="56548-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="56548-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56548-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="56548-115">Methods</span></span>

<span data-ttu-id="56548-116">Die **iameinterrorlog** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="56548-116">The **IAMSetErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="56548-117">Methode</span><span class="sxs-lookup"><span data-stu-id="56548-117">Method</span></span>                                               | <span data-ttu-id="56548-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56548-118">Description</span></span>                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="56548-119">**\_ErrorLog erhalten**</span><span class="sxs-lookup"><span data-stu-id="56548-119">**get\_ErrorLog**</span></span>](iamseterrorlog-get-errorlog.md) | <span data-ttu-id="56548-120">Ruft das aktuelle Fehlerprotokoll für dieses-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="56548-120">Retrieves the current error log for this object.</span></span><br/> |
| [<span data-ttu-id="56548-121">**\_ErrorLog ablegen**</span><span class="sxs-lookup"><span data-stu-id="56548-121">**put\_ErrorLog**</span></span>](iamseterrorlog-put-errorlog.md) | <span data-ttu-id="56548-122">Gibt ein Fehlerprotokoll für das-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="56548-122">Specifies an error log for the object.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="56548-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56548-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56548-124">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="56548-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="56548-125">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="56548-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="56548-126">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56548-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56548-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56548-127">Requirements</span></span>



| <span data-ttu-id="56548-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56548-128">Requirement</span></span> | <span data-ttu-id="56548-129">Wert</span><span class="sxs-lookup"><span data-stu-id="56548-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56548-130">Header</span><span class="sxs-lookup"><span data-stu-id="56548-130">Header</span></span><br/>  | <dl> <span data-ttu-id="56548-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="56548-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="56548-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56548-132">Library</span></span><br/> | <dl> <span data-ttu-id="56548-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="56548-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
