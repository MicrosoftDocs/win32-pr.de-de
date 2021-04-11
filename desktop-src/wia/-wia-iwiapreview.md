---
description: Die iwiapreview-Schnittstelle speichert ungefilterte Bilder intern zwischen und übergibt sie durch Bild Verarbeitungs Filter.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Iwiapreview-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214655"
---
# <a name="iwiapreview-interface"></a><span data-ttu-id="2e45b-103">Iwiapreview-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2e45b-103">IWiaPreview interface</span></span>

<span data-ttu-id="2e45b-104">Die **iwiapreview** -Schnittstelle speichert ungefilterte Bilder intern zwischen und übergibt sie durch Bild Verarbeitungs Filter.</span><span class="sxs-lookup"><span data-stu-id="2e45b-104">The **IWiaPreview** interface caches unfiltered images internally and passes them through image processing filters.</span></span>

## <a name="members"></a><span data-ttu-id="2e45b-105">Member</span><span class="sxs-lookup"><span data-stu-id="2e45b-105">Members</span></span>

<span data-ttu-id="2e45b-106">Die **iwiapreview** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2e45b-106">The **IWiaPreview** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2e45b-107">**Iwiapreview** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2e45b-107">**IWiaPreview** also has these types of members:</span></span>

-   [<span data-ttu-id="2e45b-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="2e45b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2e45b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="2e45b-109">Methods</span></span>

<span data-ttu-id="2e45b-110">Die **iwiapreview** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2e45b-110">The **IWiaPreview** interface has these methods.</span></span>



| <span data-ttu-id="2e45b-111">Methode</span><span class="sxs-lookup"><span data-stu-id="2e45b-111">Method</span></span>                                                  | <span data-ttu-id="2e45b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e45b-112">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e45b-113">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="2e45b-113">**Clear**</span></span>](-wia-iwiapreview-clear.md)                 | <span data-ttu-id="2e45b-114">Gibt das ungefilterte Bild frei, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="2e45b-114">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="2e45b-115">Außerdem wird der Bild Verarbeitungs Filter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="2e45b-115">It also releases the image processing filter.</span></span> <br/>          |
| [<span data-ttu-id="2e45b-116">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="2e45b-116">**DetectRegions**</span></span>](-wia-iwiapreview-detectregions.md) | <span data-ttu-id="2e45b-117">Ruft den Treiber Segmentierungs Filter auf und übergibt das ungefilterte Bild, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird, an den Filter.</span><span class="sxs-lookup"><span data-stu-id="2e45b-117">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span> <br/> |
| [<span data-ttu-id="2e45b-118">**Getnewpreview**</span><span class="sxs-lookup"><span data-stu-id="2e45b-118">**GetNewPreview**</span></span>](-wia-iwiapreview-getnewpreview.md) | <span data-ttu-id="2e45b-119">Speichert das vom Treiber zurückgegebene ungefilterte Bild intern zwischen.</span><span class="sxs-lookup"><span data-stu-id="2e45b-119">Caches internally the unfiltered image returned from the driver.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="2e45b-120">**Updatepreview**</span><span class="sxs-lookup"><span data-stu-id="2e45b-120">**UpdatePreview**</span></span>](-wia-iwiapreview-updatepreview.md) | <span data-ttu-id="2e45b-121">Ruft das ungefilterte Bild ab, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="2e45b-121">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="2e45b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e45b-122">Remarks</span></span>

<span data-ttu-id="2e45b-123">Dieser Filter wird automatisch von der [**iwiatransfer::D ownload**](-wia-iwiatransfer-download.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2e45b-123">This filter is called automatically by the [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) method.</span></span>

<span data-ttu-id="2e45b-124">Die **iwiapreview** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.</span><span class="sxs-lookup"><span data-stu-id="2e45b-124">The **IWiaPreview** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="2e45b-125">IUnknown-Methoden</span><span class="sxs-lookup"><span data-stu-id="2e45b-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="2e45b-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e45b-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="2e45b-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="2e45b-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="2e45b-128">Gibt Zeiger auf unterstützte Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="2e45b-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="2e45b-129">IUnknown:: adressf</span><span class="sxs-lookup"><span data-stu-id="2e45b-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="2e45b-130">Inkrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="2e45b-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="2e45b-131">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="2e45b-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="2e45b-132">Dekrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="2e45b-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="2e45b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e45b-133">Requirements</span></span>



| <span data-ttu-id="2e45b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e45b-134">Requirement</span></span> | <span data-ttu-id="2e45b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="2e45b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e45b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e45b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2e45b-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e45b-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2e45b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e45b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2e45b-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e45b-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2e45b-140">Header</span><span class="sxs-lookup"><span data-stu-id="2e45b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e45b-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e45b-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e45b-142">IDL</span><span class="sxs-lookup"><span data-stu-id="2e45b-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e45b-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e45b-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
