---
description: Die iwiasegmentationfilter-Schnittstelle erkennt Unterbereiche eines bildstreams und stellt separate IWiaItem2 Items für jede dar.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Iwiasegmentationfilter-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862675"
---
# <a name="iwiasegmentationfilter-interface"></a><span data-ttu-id="3b68a-103">Iwiasegmentationfilter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b68a-103">IWiaSegmentationFilter interface</span></span>

<span data-ttu-id="3b68a-104">Die **iwiasegmentationfilter** -Schnittstelle erkennt Unterbereiche eines bildstreams und stellt separate [**IWiaItem2**](-wia-iwiaitem2.md) Items für jede dar.</span><span class="sxs-lookup"><span data-stu-id="3b68a-104">The **IWiaSegmentationFilter** interface detects sub-regions of an image stream and makes separate [**IWiaItem2**](-wia-iwiaitem2.md) items for each.</span></span>

## <a name="members"></a><span data-ttu-id="3b68a-105">Member</span><span class="sxs-lookup"><span data-stu-id="3b68a-105">Members</span></span>

<span data-ttu-id="3b68a-106">Die **iwiasegmentationfilter** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3b68a-106">The **IWiaSegmentationFilter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3b68a-107">**Iwiasegmentationfilter** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3b68a-107">**IWiaSegmentationFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="3b68a-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="3b68a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3b68a-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="3b68a-109">Methods</span></span>

<span data-ttu-id="3b68a-110">Die **iwiasegmentationfilter** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3b68a-110">The **IWiaSegmentationFilter** interface has these methods.</span></span>



| <span data-ttu-id="3b68a-111">Methode</span><span class="sxs-lookup"><span data-stu-id="3b68a-111">Method</span></span>                                                             | <span data-ttu-id="3b68a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b68a-112">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b68a-113">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="3b68a-113">**DetectRegions**</span></span>](-wia-iwiasegmentationfilter-detectregions.md) | <span data-ttu-id="3b68a-114">Bestimmt die Unterbereiche eines Bilds, das auf dem flachen Platen angeordnet ist, sodass jede Unterregion in einem separaten Bildelement abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b68a-114">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b68a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b68a-115">Remarks</span></span>

<span data-ttu-id="3b68a-116">Eine Anwendung sollte [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) verwenden, um eine neue Instanz des Segmentierungs Filters zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b68a-116">An application should use [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) to create a new instance of the segmentation filter.</span></span> <span data-ttu-id="3b68a-117">Eine Anwendung ruft diese Funktion in der Regel auf, bevor das Vorschaufenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3b68a-117">An application typically calls this function before displaying its preview window.</span></span>

<span data-ttu-id="3b68a-118">Verwenden Sie bei der Implementierung dieses Filters [**IWiaItem2:: kreatechilditem**](-wia-iwiaitem2-createchilditem.md) , um die untergeordneten Elemente zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b68a-118">When implementing this filter, use [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) to create the child items.</span></span> <span data-ttu-id="3b68a-119">Die Anwendung sollte die **Eigenschaften \_ \_ \_ Werte der übergeordneten Kopie** an den *ikreationflags* -Parameter übergeben, um sicherzustellen, dass Eigenschaften wie das Bildformat und die Auflösung in dem neu erstellten untergeordneten Element identisch sind, wie im übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="3b68a-119">The application should pass **COPY\_PARENT\_PROPERTY\_VALUES** to the *ICreationFlags* parameter to ensure that properties such as image format and resolution is the same in the newly created child as in the parent item.</span></span>

<span data-ttu-id="3b68a-120">Ein Segmentierungs Filter muss alle Bildformate unterstützen, mit denen der Treiber, mit dem er verwendet wird, unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b68a-120">A segmentation filter must support all the image formats that the driver it is used with supports.</span></span> <span data-ttu-id="3b68a-121">Der von Microsoft bereitgestellte Filter unterstützt Bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) und Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="3b68a-121">The Microsoft provided filter supports bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="3b68a-122">Der Segmentierungs Filter sollte nur für Filterelemente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b68a-122">The segmentation filter should be used only on film and flatbed scanner items.</span></span> <span data-ttu-id="3b68a-123">Bei der Überprüfung des Filters kommt es bei einem Scanner häufig zu festgelegten Rahmen. in diesem Fall hat der Treiber die untergeordneten Elemente erstellt, und die Anwendung sollte den Segmentierungs Filter nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3b68a-123">For film scanning, a scanner often comes with fixed frames in which case the driver created the child items and the application should not invoke the segmentation filter.</span></span>

<span data-ttu-id="3b68a-124">Die **iwiasegmentationfilter** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.</span><span class="sxs-lookup"><span data-stu-id="3b68a-124">The **IWiaSegmentationFilter** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="3b68a-125">IUnknown-Methoden</span><span class="sxs-lookup"><span data-stu-id="3b68a-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="3b68a-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b68a-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3b68a-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="3b68a-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="3b68a-128">Gibt Zeiger auf unterstützte Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="3b68a-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="3b68a-129">IUnknown:: adressf</span><span class="sxs-lookup"><span data-stu-id="3b68a-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="3b68a-130">Inkrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="3b68a-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="3b68a-131">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="3b68a-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="3b68a-132">Dekrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="3b68a-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="3b68a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b68a-133">Requirements</span></span>



| <span data-ttu-id="3b68a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b68a-134">Requirement</span></span> | <span data-ttu-id="3b68a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3b68a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b68a-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b68a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3b68a-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b68a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3b68a-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b68a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3b68a-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b68a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3b68a-140">Header</span><span class="sxs-lookup"><span data-stu-id="3b68a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b68a-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b68a-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b68a-142">IDL</span><span class="sxs-lookup"><span data-stu-id="3b68a-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b68a-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b68a-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
