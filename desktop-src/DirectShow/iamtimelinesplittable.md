---
description: Die iamtimelinesplicustom-Schnittstelle teilt ein Zeitachsen Objekt in DirectShow-Bearbeitungs Diensten (de). Quellen, Effekte, Übergänge und Spuren implementieren diese Schnittstelle.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Iamtimelinesplicustom-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361281"
---
# <a name="iamtimelinesplittable-interface"></a><span data-ttu-id="fea34-104">Iamtimelinesplicustom-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fea34-104">IAMTimelineSplittable interface</span></span>

> [!Note]  
> <span data-ttu-id="fea34-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fea34-105">\[Deprecated.</span></span> <span data-ttu-id="fea34-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="fea34-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fea34-107">Die- `IAMTimelineSplittable` Schnittstelle teilt ein Zeitachsen Objekt in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="fea34-107">The `IAMTimelineSplittable` interface splits a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="fea34-108">Quellen, Effekte, Übergänge und Spuren implementieren diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fea34-108">Sources, effects, transitions, and tracks implement this interface.</span></span>

## <a name="members"></a><span data-ttu-id="fea34-109">Member</span><span class="sxs-lookup"><span data-stu-id="fea34-109">Members</span></span>

<span data-ttu-id="fea34-110">Die **iamtimelinesplicustom** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fea34-110">The **IAMTimelineSplittable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fea34-111">**Iamtimelinesplicustom** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fea34-111">**IAMTimelineSplittable** also has these types of members:</span></span>

-   [<span data-ttu-id="fea34-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="fea34-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fea34-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="fea34-113">Methods</span></span>

<span data-ttu-id="fea34-114">Die **iamtimelinesplicustom** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fea34-114">The **IAMTimelineSplittable** interface has these methods.</span></span>



| <span data-ttu-id="fea34-115">Methode</span><span class="sxs-lookup"><span data-stu-id="fea34-115">Method</span></span>                                             | <span data-ttu-id="fea34-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fea34-116">Description</span></span>                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fea34-117">**Splitat**</span><span class="sxs-lookup"><span data-stu-id="fea34-117">**SplitAt**</span></span>](iamtimelinesplittable-splitat.md)   | <span data-ttu-id="fea34-118">Teilt das Objekt zum angegebenen Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="fea34-118">Splits the object at the specified time.</span></span><br/>                                                  |
| [<span data-ttu-id="fea34-119">**SplitAt2**</span><span class="sxs-lookup"><span data-stu-id="fea34-119">**SplitAt2**</span></span>](iamtimelinesplittable-splitat2.md) | <span data-ttu-id="fea34-120">Teilt das Objekt zum angegebenen Zeitpunkt, angegeben als [**ref-Zeit**](reftime.md) -Wert.</span><span class="sxs-lookup"><span data-stu-id="fea34-120">Splits the object at the specified time, specified as a [**REFTIME**](reftime.md) value.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fea34-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fea34-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fea34-122">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fea34-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fea34-123">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="fea34-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fea34-124">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fea34-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fea34-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fea34-125">Requirements</span></span>



| <span data-ttu-id="fea34-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fea34-126">Requirement</span></span> | <span data-ttu-id="fea34-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fea34-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fea34-128">Header</span><span class="sxs-lookup"><span data-stu-id="fea34-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fea34-129"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fea34-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fea34-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fea34-130">Library</span></span><br/> | <dl> <span data-ttu-id="fea34-131"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="fea34-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
